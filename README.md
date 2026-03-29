# leetcode---10
Regular Expression Matchin
Code in Java

 public class Solution {uuuuu
    public boolean isMatch(String s, String p) {
        if (p.isEmpty()) {
            return s.isEmpty();nnnnppp
        }nnñn

        boolean firstMatch = (!s.isEmpty() &&
                              (s.charAt(0) == p.charAt(0) || p.charAt(0) == '.'));
m
        if (p.length() >= 2 && p.charAt(1) == '*') {
            return (isMatch(s, p.substring(2)) ||
                    (firstMatch && isMatch(s.substring(1), p)));
        } else {
            return firstMatch && isMatch(s.substring(1), p.substring(1));
        }
    }
}
hhh
