# OOP-Ali
import java.util.ArrayList;
import java.util.Iterator;
import java.util.Scanner;

public class TestIterator {
    public static void main(String[] args) {
        System.out.println("****Record studentS name****");
        //objects
        ArrayList<String> students = new ArrayList<>();
        Scanner scanner = new Scanner(System.in);
        Iterator<String> iterator = students.iterator();

        //get data from user
        System.out.println("How many students:");
        int numOFStudents = scanner.nextInt();
        scanner.nextLine();
//populate the ArrayList.
        for (int i = 0; i < numOFStudents; i++) {
            System.out.println("Enter a student’s name");
            String name = scanner.nextLine();
            students.add(name);
        }
        //Testing
        System.out.println(students);
        //  create and Use iterator to print names.®
        System.out.println("****List of all students in uppercase****");
        while (iterator.hasNext()) {
            String student = iterator.next();
            System.out.println(student.toUpperCase());
        }
    }
}
