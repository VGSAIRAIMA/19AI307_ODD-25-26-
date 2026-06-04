# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create an Article class where changes to the content are saved as mementos. Let the user view and restore any saved version.

For example:

Input	Result
3
Initial draft
Revised content
Final article version
2
Final article version

## AIM:
To implement the Memento Design Pattern for saving and restoring different versions of an article.

## ALGORITHM :
1. Start the program execution.
2. Create classes Article, ArticleMemento, and ArticleHistory to implement the Memento Design Pattern.
3. Read the article versions from the user and create snapshots for each version.
4. Store the created snapshots in the ArticleHistory object.
5. Read the version number that needs to be restored.
6. Retrieve the corresponding snapshot from the history and display the stored article content.
7. Stop the program execution.
## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: V G SAIRAIMA
RegisterNumber:  212225040359
*/
```

## SOURCE CODE:
```
import java.util.*;

class Article {
    private String content;
    private ArticleHistory historyobj;
    public ArticleMemento snapShot(String msg){
        this.content =msg;
        return new ArticleMemento(msg);
    }
    public void save(ArticleMemento obj,ArticleHistory history){
        this.historyobj = history;
        historyobj.storeSnapShots(obj);
    }
    public void searchData(int n){
        ArticleMemento searchedobj = historyobj.returnSearchedData(n);//here is where i get obj
        if(searchedobj!=null){
        fetchData(searchedobj);}
        else{
            System.out.print("Invalid version");
        }
    }
    public void fetchData(ArticleMemento obj){
        this.content = obj.getContent();
        System.out.print(content);
    }
}

class ArticleMemento {
    private String content;
    public ArticleMemento(String msg){
        this.content = msg;
    }
    public String getContent(){
        return content;
    }
    
}

class ArticleHistory {
    List<ArticleMemento> data= new ArrayList<>();
    public void storeSnapShots(ArticleMemento obj){
        data.add(obj);
    }
    public ArticleMemento returnSearchedData(int n){
        for(int i =0;i<data.size();i++){
            if(i==n){
                return data.get(i); 
            }
        }
        return null;
    }
    
    
}

public class ArticleManager {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        in.nextLine();
        Article article = new Article();
        ArticleHistory history = new ArticleHistory();
        for (int i=0;i<n;i++){
            String msg = in.nextLine();
            ArticleMemento snapshot=article.snapShot(msg);//here i store the content then the snapshot then i return this to snapshot obj
            article.save(snapshot,history);
        }
        int no=in.nextInt();
        article.searchData(no);
        

        in.close();
    }
}

```

## OUTPUT:
![IMAGE](https://github.com/VGSAIRAIMA/19AI307_ODD-25-26-/blob/main/19AI307_JAVA(25-26)/Module-04/DAY-5/Screenshot%202026-06-04%20173334.png)
## RESULT:
The program successfully implements the Memento Design Pattern by saving multiple versions of an article and restoring the requested version from the stored snapshots.
