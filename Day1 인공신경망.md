

- ๐ DAY1: Neural Network (NN) Foundation

  - **ํผ์ํธ๋ก (Perceptron)**: ์ ๊ฒฝ๋ง์ ์ด๋ฃจ๋ ๊ฐ์ฅ **๊ธฐ๋ณธ ๋จ์**

    - ์ด๊ธฐ ํํ์ ์ธ๊ณต ์ ๊ฒฝ๋ง์ผ๋ก **๋ค์์ ์๋ ฅ**์ผ๋ก๋ถํฐ **ํ๋์ ๊ฒฐ๊ณผ**๋ฅผ ๋ด๋ณด๋ด๋ ์๊ณ ๋ฆฌ์ฆ

    - ํผ์ํธ๋ก  ๊ทธ๋ฆผ

      ![image-20210810154954858](https://user-images.githubusercontent.com/76864400/128843479-db2c8580-0463-4a8e-9dcd-b5ed615efde2.png)

      

      - x: ์๋ ฅ๊ฐ, W: ๊ฐ์ค์น, y: ์ถ๋ ฅ๊ฐ

      - **๊ฐ์ค์น**: ์ ๊ฒฝ ์ธํฌ ๋ด๋ฐ์์์ **์ ํธ๋ฅผ ์ ๋ฌ**ํ๋ ์ถ์ญ๋๊ธฐ์ ์ญํ  ํจ

        - ๊ฐ์ค์น์ ๊ฐ์ด ํฌ๋ฉด ํด์๋ก ํด๋น ์๋ ฅ ๊ฐ์ด ์ค์ ->  ๊ฐํ ์ ํธ ๋ณด๋

      - ๊ฐ ์๋ ฅ๊ฐ์ด ๊ฐ์ค์น์ ๊ณฑํด์ ธ ์ธ๊ณต ๋ด๋ฐ์ ๋ณด๋ด์ง๊ณ , ๊ฐ ์๋ ฅ๊ฐ๊ณผ ๊ทธ์ ํด๋น๋๋ ๊ฐ์ค์น์ ๊ณฑ์ ์ ์ฒด ํฉ์ด ์๊ณ์น(threshold)๋ฅผ ๋์ผ๋ฉด ์ข์ฐฉ์ง์ ์๋ ์ธ๊ณต ๋ด๋ฐ์ ์ถ๋ ฅ ์ ํธ๋ก 1์ ์ถ๋ ฅ, ์๋๋ฉด 0์ ์ถ๋ ฅ 

        ![image-20210810173107878](https://user-images.githubusercontent.com/76864400/128843482-391f9536-aee9-4567-9659-2b8fb1a1fb3c.png)

        -> ์ ์์์ ์ธํ๋ ์๊ณ์น(threshold ์๋ฏธ)

      - ์ ์์์ ์๊ณ์น๋ฅผ ์ข๋ณ์ผ๋ก ๋๊ธฐ๊ณ  ํธํฅ(bias)์ผ๋ก ํํ ๊ฐ๋ฅ

        ![image-20210810173435493](https://user-images.githubusercontent.com/76864400/128843484-90df368b-180c-4ac4-a175-271cc737600d.png)

      - ๊ณ๋จ ํจ์(Step Function)

        ![image-20210810173043531](https://user-images.githubusercontent.com/76864400/128843480-e71b2089-d449-4262-9a4e-191121ce794e.png)

      - ๋จ์ํ ๋ผ๋ฆฌ๊ฒ์ดํธ๋ก ๋ณธ **๋จ์ธต ํผ์ํธ๋ก **

        - AND GATE: ๋ ๊ฐ์ ์๋ ฅ ๊ฐ์ด ๋ชจ๋ 1์ธ ๊ฒฝ์ฐ์๋ง ์ถ๋ ฅ๊ฐ์ด 1์ด ๋์ค๋ ๊ตฌ์กฐ
        - NAND GATE: AND GATE ๊ฒฐ๊ณผ์ ๋ฐ๋(NOT AND), ๋ ๊ฐ์ ์๋ ฅ๊ฐ์ด 1์ธ ๊ฒฝ์ฐ์๋ง ์ถ๋ ฅ๊ฐ์ด 0์ด ๋์ค๋ ๊ตฌ์กฐ
        - OR GATE: ๋ ๊ฐ์ ์๋ ฅ์ด ๋ชจ๋ 0์ธ ๊ฒฝ์ฐ์ ์ถ๋ ฅ๊ฐ์ด 0์ด๊ณ  ๋๋จธ์ง ๊ฒฝ์ฐ์๋ ๋ชจ๋ ์ถ๋ ฅ๊ฐ์ด 1์ด ๋์ค๋ ๊ตฌ์กฐ
        - ๋จ์ธต ํผ์ํธ๋ก ์ ํ์ 
          - ๋จ์ธต ํผ์ํธ๋ก ์ผ๋ก๋ XOR ๋ฌธ์ (๋์ด ์๋ก ๋ค๋ฅผ ๋๋ง 1์ ์ถ๋ ฅ, ๋ฐฐํ์  ๋ผ๋ฆฌํฉ) ํด๊ฒฐ ๋ถ๊ฐ -> ํ์ง๋ง ์๋์ธต ๋๋ฆฌ๋ฉด (๋ค์ธต) ํ์  ๋ณด์ ๊ฐ๋ฅ

      - **๋ค์ธต ํผ์ํธ๋ก **

        - ์๋ ฅ์ธต๊ณผ ์ถ๋ ฅ์ธต ์ฌ์ด์ ์กด์ฌํ๋ ์ธต์ธ **์๋์ธต**์ด ์กด์ฌ

        - ๋ค์ธต ํผ์ํธ๋ก ์ผ๋ก AND, NAND, OR ๊ฒ์ดํธ๋ฅผ ์กฐํฉํ์ฌ XOR ๊ฒ์ดํธ๋ฅผ ๊ตฌํ

          ![image-20210810174728190](https://user-images.githubusercontent.com/76864400/128843456-4b296902-c019-4333-9b5f-8d4df084cfdd.png)

        

  - **์ธ๊ณต์ ๊ฒฝ๋ง(Artificial Neural Networks, ANN)**: ์ธ๊ฐ์ **๋ด๋ฐ ๊ตฌ์กฐ**๋ฅผ ๋ณธ๋  ๋ง๋  **๊ธฐ๊ณํ์ต ๋ชจ๋ธ**, ์ธ๊ฐ์ ์ ๊ฒฝ์ธํฌ๋ฅผ ๋ชจ๋ธ๋งํด ๊ธฐ๊ณ๊ฐ ํ์ตํ๋ ๊ฒ

    - **์ ๊ฒฝ์ธํฌ(๋ด๋ฐ)**: ์ ๊ฒฝ๊ณ๋ฅผ ํ์ฑํ๋ ์ธํฌ๋ก, ์ ๊ธฐ์ ์ธ ์ ํธ๋ก ์๋ก ํต์ ํ๋ฉฐ ์ ๋ณด ์ ์ฅ

    - **์ ๊ฒฝ์ธํฌ(๋ด๋ฐ)** ๊ทธ๋ฆผ 

      - ๋ด๋ฐ์ ๊ฐ์ง๋๊ธฐ(dendrites)์์ ์ ํธ๋ฅผ ๋ฐ์๋ค์ด๊ณ , ์ ํธ๊ฐ ์ผ์ ์น ์ด์์ ํฌ๊ธฐ๋ฅผ ๊ฐ์ง๋ฉด ์ถ์ญ๋๊ธฐ(axon hillock) ๋ฅผ ํตํด ์ ํธ ์ ๋ฌ
        - Cellbody(์ ๊ฒฝ์ธํฌ์ฒด): ์ฐ์ฐ์ ํจ

      ![image-20210810154140881](https://user-images.githubusercontent.com/76864400/128843475-ea90a4ff-025d-4754-9d7e-4633e9f9958d.png)

    - **์ ๊ฒฝ๋ง ์ธต**

      - **์๋ ฅ์ธต**(input layer์ ๋ธ๋ ๊ฐ์: feature ์)

        - ๋ฐ์ดํฐ์์ผ๋ก๋ถํฐ ์๋ ฅ ๋ฐ์
        - ์๋ ฅ ๋ณ์์ ์ = ์๋ ฅ ๋ธ๋์ ์
        - ์๋ ฅ์ธต์ ์ด๋ค ๊ณ์ฐ๋ ์ํํ์ง ์์
        - ์ ๊ฒฝ๋ง์ ์ธต์๋ฅผ ์ ๋ ์๋ ฅ์ธต ํฌํจํ์ง ์์

      - **์๋์ธต**(hidden layer)

        - ๊ณ์ฐ ์ผ์ด๋๋ ์ธต์ด ๋ ์ด์์ธ ์ ๊ฒฝ๋ง์ ๋ค์ธต ์ ๊ฒฝ๋ง

        - ๊ณ์ฐ ์๋ ์๋ ฅ์ธต๊ณผ ๋ง์ง๋ง ์ถ๋ ฅ์ธต ์ฌ์ด์ ์๋ ์ธต๋ค์ ์๋์ธต

        - ์๋์ธต์ ์๋ ๊ณ์ฐ ๊ฒฐ๊ณผ๋ฅผ ์ฌ์ฉ์๊ฐ ๋ณผ ์ ์์

        - ๋ฅ๋ฌ๋์ ์ฌ์ค ๋ ๊ฐ ์ด์์ ์๋์ธต์ ๊ฐ์ง ์ ๊ฒฝ๋ง(์ฌ์ธต ์ ๊ฒฝ๋ง)

          -> ์๋ ฅ์ธต์ ์ ์ธํ๊ณ  ์ธ๋ณด๋ฉด 3๊ฐ ์ด์์ layer ๊ฐ๊ณ  ์๋ ์ ๊ฒฝ๋ง ์๋ฏธํจ

      - **์ถ๋ ฅ์ธต**(output layer์ ๋ธ๋ ๊ฐ์: ํ๊ฒ ๊ฐ, ํด๋์ค ์)

        - ํ์ฑํจ์๊ฐ ์กด์ฌํ๋๋ฐ ํ์ฑํํจ์๋ ํ๊ณ ์ํ๋ ๋ฌธ์ ์ ๋ฐ๋ผ ๋ค๋ฅธ ์ข๋ฅ ์ฌ์ฉ

        - ํ๊ท๋ฌธ์ ์์ ์์ธกํ  ๋ชฉํ ๋ณ์๊ฐ ์ค์๊ฐ์ธ ๊ฒฝ์ฐ ํ์ฑํํจ์๊ฐ ํ์ ์์ 

          โ ์ถ๋ ฅ๋ธ๋์ ์๋ ์ถ๋ ฅ๋ณ์์ ๊ฐ์

        - ์ด์ง ๋ถ๋ฅ ๋ฌธ์ ์ ๊ฒฝ์ฐ, ์๊ทธ๋ชจ์ด๋ ํจ์๋ฅผ ์ฌ์ฉํด ์ถ๋ ฅ์ ํ๋ฅ ๊ฐ์ผ๋ก ๋ณํํด ํด๋์ค ๊ฒฐ์ ํ๋๋ก ํจ

          โ์ด์ง๋ถ๋ฅ๋ class์๊ฐ 2๊ฐ โ (0 ์๋๋ฉด 1)

          โ ๋ณดํต ๋ธ๋ 1๊ฐ โ sigmoid function ์ฌ์ฉ

        - ๋ค์ค ํด๋์ค๋ฅผ ๋ถ๋ฅํ๋ ๊ฒฝ์ฐ ์ถ๋ ฅ์ธต ๋ธ๋๊ฐ ๋ถ๋ฅ ์ ๋งํผ ์กด์ฌํ๋ฉฐ ์ํํธ๋งฅ์ค ํจ์๋ฅผ ํ์ฑํ ํจ์๋ก ์ฌ์ฉ

      

    - **ํ์ฑํ ํจ์(Activation Function)**

      - ์๋ ฅ๋ ๋ฐ์ดํฐ์ ๊ฐ์ค ํฉ์ ์ถ๋ ฅ ์ ํธ๋ก ๋ณํํ๋ ํจ์
      - ํ์ฑํ ํจ์๋ ๋น์ ํ ํจ์

      ![image-20210810180024355](https://user-images.githubusercontent.com/76864400/128843462-f836df76-15c0-4e57-87b7-7df23a424dd2.png)

      - **๊ณ๋จ ํจ์(step function)**

        ![image-20210810180156993](https://user-images.githubusercontent.com/76864400/128843464-81e3b538-789b-4a28-b5a6-5c7d979e15f8.png)

        - ๊ฑฐ์ ์ฌ์ฉ๋์ง ์์ง๋ง, ํผ์ํธ๋ก ์ ํตํด ์ฒ์์ผ๋ก ์ธ๊ณต ์ ๊ฒฝ๋ง ๋ฐฐ์ธ ๋ ๊ฐ์ฅ ์ฒ์ ์ ํ๋ ํ์ฑํ ํจ์

        - 0๋ณด๋ค ํฐ ๊ฒฝ์ฐ 1 ์ถ๋ ฅ, 0๋ณด๋ค ์์ ๊ฒฝ์ฐ 0์ ์ถ๋ ฅํ๋ ํจ์

      - **์๊ทธ๋ชจ์ด๋ ํจ์(sigmoid function)**

        ![image-20210810180609931](https://user-images.githubusercontent.com/76864400/128843467-16dff423-8380-485f-9e1d-0728a263aeed.png)

        - 0~1์ฌ์ด ์ถ๋ ฅํ๋ ํจ์

      - **๋ ๋ฃจ ํจ์(ReLU function)**

        ![image-20210810180819229](https://user-images.githubusercontent.com/76864400/128843471-159bf8fa-6fe3-4402-8394-d53c61e0d5e3.png)

        - ์ธ๊ณต ์ ๊ฒฝ๋ง์์ ๊ฐ์ฅ ์ต๊ณ ์ ์ธ๊ธฐ๋ฅผ ์ป๊ณ  ์๋ ํจ์
        - ์๋์ธต์์ ReLUํจ์๋ค์ ์ฌ์ฉํ๋ ๊ฒ์ด ์ผ๋ฐ์ 
        - ์์๋ฅผ ์๋ ฅํ๋ฉด 0์ ์ถ๋ ฅํ๊ณ , ์์๋ฅผ ์๋ ฅํ๋ฉด ์๋ ฅ๊ฐ์ ๊ทธ๋๋ก ๋ฐํ
        - 0๋ณด๋ค ํฌ๋ฉด ์๊ธฐ ์์  ๋ด๋ณด๋ด๊ณ (linear), 0๋ณด๋ค ์์ผ๋ฉด 0์ ์ถ๋ ฅํ๋ ํจ์

      - **์ํํธ๋งฅ์ค ํจ์(Softmx function)**

        ![image-20210810181001758](https://user-images.githubusercontent.com/76864400/128843474-984c3178-d401-4a66-bd16-4a7f50a776b3.png)

        - ์๊ทธ๋ชจ์ด๋ ํจ์์ฒ๋ผ ์ถ๋ ฅ์ธต์ ๋ด๋ฐ์์ ์ฃผ๋ก ์ฌ์ฉ
        - ์๊ทธ๋ชจ์ด๋ ํจ์๊ฐ ์ด์ง ๋ถ๋ฅ ๋ฌธ์ (Binary Classification)์ ์ฌ์ฉ๋๋ค๋ฉด, ์ํํธ๋งฅ์ค ํจ์๋ ๋ค์ค ํด๋์ค ๋ถ๋ฅ ๋ฌธ์ (MultiClass Classification) ์ ์ฃผ๋ก ์ฌ์ฉ๋จ

