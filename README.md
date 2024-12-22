# 25PR
# 25 Практика
# Задание 4
```
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class EmailValidator {
    private static final String EMAIL_REGEX =
            "^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$";

    public static boolean isValidEmail(String email) {
        Pattern pattern = Pattern.compile(EMAIL_REGEX);
        Matcher matcher = pattern.matcher(email);
        return matcher.matches();
    }

    public static void main(String[] args) {
        String[] testEmails = {
            "user@example.com",
            "root@localhost",
            "myhost@@@com.ru",
            "@my.ru",
            "Julia String"
        };

        for (String email : testEmails) {
            System.out.println(email + ": " + (isValidEmail(email) ? "Корректный" : "Некорректный"));
        }
    }
}
```
# Задание 5
```
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class PasswordValidator {
    private static final String PASSWORD_REGEX =
            "^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)[a-zA-Z\d_]{8,}$";

    public static boolean isStrongPassword(String password) {
        Pattern pattern = Pattern.compile(PASSWORD_REGEX);
        Matcher matcher = pattern.matcher(password);
        return matcher.matches();
    }

    public static void main(String[] args) {
        String[] testPasswords = {
            "F032_Password",
            "TrySpy1",
            "smart_pass",
            "A007"
        };

        for (String password : testPasswords) {
            System.out.println(password + ": " + (isStrongPassword(password) ? "Надежный" : "Ненадежный"));
        }
    }
}
```
