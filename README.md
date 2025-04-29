# Installing the library
- The android chatbot sdk is hosted on a private github site.
- To access the sdk add the below to repository to the list of repositories in the root build.gradle file

    ```
    maven {
        url "https://arjavdave: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@maven.pkg.github.com/kevit-in/chatbot-kotlin"
    }
    ```

- In your module's build.gradle file add the below dependency

    ```
    implementation "com.kevit:chatbot-kotlin:1.0.5"
    ```

- Sync the project

# import the Packages
In your preferred Activity import the relevant packages as below
    
    ```
    import com.kevit.chatbotkotlin.API.ChatBotDesign
    import com.kevit.chatbotkotlin.API.Style
    import com.kevit.chatbotkotlin.ChatBot
    import com.kevit.chatbotkotlin.ChatBotModel
    ```

# Initialize bot design (Optional)
    ```
    val botDesign = ChatBotDesign(
                "Hello World",
                "https://cdn-icons-png.freepik.com/256/4712/4712015.png?semt=ais_hybrid",
                Style("#123445", "#112233"),
                Style("#112233", "#e2a445"),
                Style("#e2a445", "#112233")
            )
    ```

# Initialize User Input (Optional)
```
    val userInput = HashMap<String, String>()
    userInput["email"] = "test@123.io"
```

# Initialize the ChatBot
    ```
    val model = ChatBotModel(
        "<appId>",
        "<appSecret>",
        userInput,
        "<botUrl>",
        "<socketUrl>",
        botDesign
    )
    ```



# Initialize the ChatBot with the details
    ```
    ChatBot.getInstance().initialize(model)
    ```


# Show the ChatBot screen
    ```
    ChatBot.getInstance().show(this)
    ```
