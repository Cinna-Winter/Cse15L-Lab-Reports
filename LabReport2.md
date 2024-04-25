## Part 1

**CODE:**

import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;
import java.util.List;


class Handler implements URLHandler {
    private List<String> messages = new ArrayList<>();
    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Text Chat Starts Here!");
        } else if (url.getPath().equals("/add-message")) {
            String[] parameters = url.getQuery().split("&");
            String s = null;
            String user = null;
            for (String parameter : parameters) {
                String[] assign = parameter.split("=");
                if (assign.length > 1) {
                    if ("s".equals(assign[0])) {
                         s = assign[1];
                    } else if ("user".equals(assign[0])) {
                        user = assign[1];
                    }
                }
            }
            if (s != null && user != null) {
                String message = String.format("From user:%s: %s", user, s);
                messages.add(message);
                return String.join("\n", messages);
            }
         }
            return "404 Not Found!";
      }
}



## Part 2

## Part 3
