## Project Log: **A Conceptual Game Design Exploring the Nexus of Human Dreams and AI Image Generation**

GitHub: https://github.com/YingTao-22019022/YingTao-22019022-AdvancedProject
https://github.com/YingTao-22019022/YingTao-MScAdvancedProject

Video: https://youtu.be/z7acOiIjccU



## Level I(2023.6-2023.8)

In this stage, we mainly search relevant literature, determine the research direction, and formulate related project plans.

After making it clear that I wanted to discuss AI painting as the theme, I collected relevant news about AI painting, and also learned some attitudes about painters and artists towards AI painting through some social media.

It happened that at this time, I was playing some games related to sleep, dreams and psychology, so I wanted to combine the two ideas.

For me, it's not just about making a critical project, but I also want the project or the game to be fun.

Based on this idea, I started a series of plans and experiments.

![](.\READMEPHOTO\1280X1280.PNG)



## Level II(2023.8-2023.9)

After figuring out that I wanted to develop a 2d game using the unity engine, I started a series of studies. I also started using two AI image generation tools, stable diffusion and midijourney.

The main thing I did at this stage was to learn, I looked at bilibili and youtube for learning materials I wanted to learn, to understand the skills I might need to learn in the future development process



## Level III(2023.9-2023.10)

- Prepare questionnaire survey

  Part of the questionnaire was collected online and part was collected offline. The following is the record of the questionnaire collected online

  ![20231124232054](.\READMEPHOTO\20231124232054.png)

  ![1](.\READMEPHOTO\1.png)

  ![4](.\READMEPHOTO\2.png)

  ![2](.\READMEPHOTO\3.png)

  ![3](.\READMEPHOTO\4.png)

- Image generation

  A total of five sets of images were trained, three of which ended up in the actual game. The following is the basic data of the training, and the actual training data will be adjusted on this basis.

  （1）

  ![5](.\READMEPHOTO\5.png)

  ```
  Stable Diffusion CheckPoint
  
  realisticVisionV51
  
  Prompt
  
  Abstract,Collapsed,scared,nervous,irritable,unknown space,greyscale,<lora:江南梦 Jiangnan Dream_v1.0:1>,
  
  Negative Prompt
  
  concrete,persona,
  ```

  (2)

  ![6](.\READMEPHOTO\6.png)

  ```
  abstract,realistic,nervous,awkward,irritable,red,orange,at work,computer screen,<lora:江南梦 Jiangnan Dream_v1.0:1>,
  Steps: 28, Sampler: DPM++ 2M Karras, CFG scale: 5, Seed: 2464937496, Size: 512x512, Model hash: 7f96a1a9ca, Model: anything-v5-PrtRE, VAE hash: f921fb3f29, VAE: animevae.pt, Clip skip: 2, Lora hashes: "江南梦 Jiangnan Dream_v1.0: 06d30dd52d0d", Version: v1.6.0
  ```

  (3)

  ![7](.\READMEPHOTO\7.png)

  ```
  Collapsed characters,characters doing illogical things,nervous and irritable,red,black and white,very dark,escape,tracking,<lora:江南梦 Jiangnan Dream_v1.0:1>,
  Steps: 28, Sampler: DPM++ 2M SDE Heun Exponential, CFG scale: 5, Seed: 2825304123, Size: 512x512, Model hash: 7f96a1a9ca, Model: anything-v5-PrtRE, VAE hash: f921fb3f29, VAE: animevae.pt, Clip skip: 2, Lora hashes: "江南梦 Jiangnan Dream_v1.0: 06d30dd52d0d", Version: v1.6.0
  ```

  (4)

  ![8](.\READMEPHOTO\8.png)

  ```
  Nervous,excited,green,cyan,black and white,road,loneliness,bus stop,confused,maze,unable to communicate,<lora:江南梦 Jiangnan Dream_v1.0:1>,
  Steps: 28, Sampler: DPM++ 2M SDE Heun Exponential, CFG scale: 5, Seed: 2127477180, Size: 512x512, Model hash: 7f96a1a9ca, Model: anything-v5-PrtRE, VAE hash: f921fb3f29, VAE: animevae.pt, Clip skip: 2, Lora hashes: "江南梦 Jiangnan Dream_v1.0: 06d30dd52d0d", Version: v1.6.0
  ```

  (5)

  ![9](.\READMEPHOTO\9.png)

  ```
  dreaming, thinking, lavender, sky, grass, seaside, bright,<lora:江南梦 Jiangnan Dream_v1.0:1>,<lora:蓝色幻想_v1.0:1>,
  Steps: 28, Sampler: DPM++ 2M Karras, CFG scale: 7, Seed: 1464931037, Size: 512x512, Model hash: 7f96a1a9ca, Model: anything-v5-PrtRE, VAE hash: f921fb3f29, VAE: animevae.pt, Clip skip: 2, Lora hashes: "江南梦 Jiangnan Dream_v1.0: 06d30dd52d0d, 蓝色幻想_v1.0: a774608dcbdb", Version: v1.6.0
  ```

  

- outline

  - Abstract

  - Introduction

    - Background

      The causes of human dreams

      Principles of AI generation

      Human's negative attitude towards AI painting

    - aim

      It gives people a different perspective on ai generation

  - Related Work

    - Artist’s attitude towards AI
    - Reasons why humans are afraid of AI
    - The difference between human painting and AI generation
    - Current trends in AI painting
    - Similarities and differences between AI generation and dreams

  - Methodology

    - Questionnaire survey
    - User interviews
    - Interaction design experience design
    - unity development
    - ai image generation
    - iterative design

  - A Project Write Up

  - Evaluation & Future Work

    - This could employ user testing and testing results
    - It could employ quantitative evaluation of your work
    - It could employ critical self-reflection
    - And/or other methods (See Creative Research methods below)

  - Conclusions & Discussion

## Level IV(2023.10-2023.11)

Because my grandfather died suddenly during this period, I could not work normally for 2-3 weeks, so the actual time left for me was not much. The main difficulty in this part is the communication between unity and chatgpt. The rest of the game development wasn't too difficult for me, and it went well.

The priority was getting the API out of the way, and I bought chatgpt's paid API to keep the project going

```
public string apiKey = "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";
public string url = "https://api.openai.com/v1/chat/completions";
```

```
byte[] myData = System.Text.Encoding.UTF8.GetBytes("{ \"model\": \"gpt-3.5-turbo\", \"messages\": [{\"role\": \"system\", \"content\": \""+ promptAgo + message+ promptAfter + "\"}, {\"role\": \"user\", \"content\": \"message\"}]}");
        UnityWebRequest webRequest = UnityWebRequest.Put(url, myData);
        webRequest.method = UnityWebRequest.kHttpVerbPOST;
        webRequest.SetRequestHeader("Authorization", "Bearer " + apiKey);
        webRequest.SetRequestHeader("Content-Type", "application/json");
        yield return webRequest.SendWebRequest();
        if (webRequest.result == UnityWebRequest.Result.Success)
        {
            string response = webRequest.downloadHandler.text;
            ChatCompletion myObject = new ChatCompletion();                   
            myObject = JsonUtility.FromJson<ChatCompletion>(response);
            string content = myObject.choices[0].message.content;
            outputText.text = content;
        }
        else
        {
            //Debug.LogError("Chat request failed: " + webRequest.error);
            outputText.text = webRequest.error;
        }
```

As for the thesis, the idea is relatively clear, and the writing difficulty is not very large. At the same time, I also found relevant literature to read according to the content I want to write

After the completion of the game development, several users who participated in the questionnaire survey were invited to test the game.

Although this project was limited by time and energy issues and could not carry out in-depth iterative development, I also recorded the experience suggestions given by relevant users, hoping to have the opportunity to further improve my project in the future.
