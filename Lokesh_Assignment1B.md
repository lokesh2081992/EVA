## Assignment 1B

### What are channels and kernels?

* Channels :

  Channels can be considered as the similar feature bags/items present in an image.

  for example if we are having a RGB image, that means we are getting data from the three sensors Red, Green and Blue here red, green and blue are three different channels for an RGB image



* Kernels :

  Kernels are nothing but the filters which we use to convolute the image to the next layer, In other way we can say that with the help of kernel we are going to extract the features from the image

  

  In the below image Blue color is the input image and green one is the feature map, so for every cell in the feature map is the result of the product of a kernel/filter(shaded region on the input image i.e. blue color) on a specific region of input

  

   ![1556640416156](C:\Users\lokesh\AppData\Roaming\Typora\typora-user-images\1556640416156.png)





### Why should we only (well mostly) use 3x3 Kernels?

* Basically we will be using mostly the even number kernels since we will be able to detect middle position easily with odd numbers and using specifically 3*3 filter is most of the things are well established with 3 by 3 kernels and system will work very fast by using this



###  How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 (show calculations)

199	*	199		Input 
197	*	197	   1 - kernel
195	*	195	   2 - kernel
193	*	193	   3 - kernel
191	*	191	   4 - kernel
189	*	189	   5 - kernel
187	*	187	   6 - kernel
185	*	185	   7 - kernel
183	*	183	   8 - kernel
181	*	181	   9 - kernel
179	*	179	   10 - kernel
177	*	177	   11 - kernel
175	*	175	   12 - kernel
173	*	173	   13 - kernel
171	*	171	   14 - kernel
169	*	169	   15 - kernel
167	*	167	   16 - kernel
165	*	165	   17 - kernel
163	*	163	   18 - kernel
161	*	161	   19 - kernel
159	*	159	   20 - kernel
157	*	157	   21 - kernel
155	*	155	   22 - kernel
153	*	153	   23 - kernel
151	*	151	   24 - kernel
149	*	149	   25 - kernel
147	*	147	   26 - kernel
145	*	145	   27 - kernel
143	*	143	   28 - kernel
141	*	141	   29 - kernel
139	*	139	   30 - kernel
137	*	137	   31 - kernel
135	*	135	   32 - kernel
133	*	133	   33 - kernel
131	*	131	   34 - kernel
129	*	129	   35 - kernel
127	*	127	   36 - kernel
125	*	125	   37 - kernel
123	*	123	   38 - kernel
121	*	121	   39 - kernel
119	*	119	   40 - kernel
117	*	117	   41 - kernel
115	*	115	   42 - kernel
113	*	113	   43 - kernel
111	*	111	   44 - kernel
109	*	109	   45 - kernel
107	*	107	   46 - kernel
105	*	105	   47 - kernel
103	*	103	   48 - kernel
101	*	101	   49 - kernel
99	*	99	   50 - kernel
97	*	97	   51 - kernel
95	*	95	   52 - kernel
93	*	93	   53 - kernel
91	*	91	   54 - kernel
89	*	89	   55 - kernel
87	*	87	   56 - kernel
85	*	85	   57 - kernel
83	*	83	   58 - kernel
81	*	81	   59 - kernel
79	*	79	   60 - kernel
77	*	77	   61 - kernel
75	*	75	   62 - kernel
73	*	73	   63 - kernel
71	*	71	   64 - kernel
69	*	69	   65 - kernel
67	*	67	   66 - kernel
65	*	65	   67 - kernel
63	*	63	   68 - kernel
61	*	61	   69 - kernel
59	*	59	   70 - kernel
57	*	57	   71 - kernel
55	*	55	   72 - kernel
53	*	53	   73 - kernel
51	*	51	   74 - kernel
49	*	49	   75 - kernel
47	*	47	   76 - kernel
45	*	45	   77 - kernel
43	*	43	   78 - kernel
41	*	41	   79 - kernel
39	*	39	   80 - kernel
37	*	37	   81 - kernel
35	*	35	   82 - kernel
33	*	33	   83 - kernel
31	*	31	   84 - kernel
29	*	29	   85 - kernel
27	*	27	   86 - kernel
25	*	25	   87 - kernel
23	*	23	   88 - kernel
21	*	21	   89 - kernel
19	*	19	   90 - kernel
17	*	17	   91 - kernel
15	*	15	   92 - kernel
13	*	13	   93 - kernel
11	*	11	   94 - kernel
9	*	9	   95 - kernel
7	*	7	   96 - kernel
5	*	5	   97 - kernel
3	*	3	   98 - kernel
1	*	1	   Output