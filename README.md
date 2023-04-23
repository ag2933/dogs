# Golden Retriever
## This is a repository that shows my love towards Golden Retrievers. 

_My favorite type of dog is a golden retriever, there is a photo of a golden retriever below_


![this is a photo of a golden retriever](https://github.com/ag2933/dogs/blob/21815e7ada827c2d084f589806d7f79bd73e1efe/goldenRetrievers/Doggo.jpg)

### This is a link that contains multiple photos of Golden Retrievers

This is a site that has over [500 photos of golden retrievers](https://unsplash.com/s/photos/golden-retriever)


################## Below contains a small code that if you make a tester for it, it will print out a grade that you get on a test or quiz.

public class Grade {

    private String letterGrade;

    public Grade(String grade) {
        letterGrade = grade;
    }

    public String getLetterGrade() {
        return letterGrade;
    }



    public double getNumericGrade() {
        String letter = letterGrade.substring(0,1);
        String suffix = "";
        if (letterGrade.length() >= 2)
            suffix = letterGrade.substring(1,letterGrade.length());

        double modifier = 0;

        if (suffix.equals("-"))
            modifier = -0.3;
        else if (suffix.equals("+"))
            modifier = 0.3;
        else if (!suffix.equals(""))
            return -1;

        double grade = 0;

        if (letter.toLowerCase().equals("a"))
            grade = 4;
        else if (letter.toLowerCase().equals("b"))
            grade = 3;
        else if (letter.toLowerCase().equals("c"))
            grade = 2;
        else if (letter.toLowerCase().equals("d"))
            grade = 1;
        else if (letter.toLowerCase().equals("f"))
        {
            grade = 0;
            if (modifier != 0) return -1;
        }
        else
        {
            grade = -1;
            return grade;
        }

        // Compute numeric grade
        grade = grade + modifier;

        // There is no grade higher than an A
        if(4 < grade)
            grade = 4;

        return grade;
    }

}
