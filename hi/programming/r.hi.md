{
  "date" : "2021-09-06", 
  "keywords" :["आर", "फाइल", "एक्सटेंशन", "फाइल फॉर्मेट", "आर के पुस्तकालय", "प्रोग्रामिंग गाइड", "आर उदाहरण", "आर का कोड", "आर के पुस्तकालय", "माइक्रोसॉफ्ट आर" , "आर कोड", "आर भाषा", "आरस्टूडियो"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"आर - प्रोग्रामिंग भाषा फ़ाइल",
  "description":"आर फ़ाइल प्रारूप और एपीआई के बारे में जानें जो आर फाइलें बना और खोल सकते हैं।",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## आर फाइल क्या है?

एक्सटेंशन वाली एक फ़ाइल .r प्रोग्रामिंग भाषा R से संबंधित है। यह भाषा सांख्यिकीय कंप्यूटिंग के लिए निर्दिष्ट है और सांख्यिकीविदों के समुदाय के बीच लोकप्रिय है। डेटा विश्लेषण और सांख्यिकीय सॉफ़्टवेयर का विकास डेटा खनन के क्षेत्र में इस भाषा द्वारा की जाने वाली दो मुख्य श्रेणियां हैं। इस भाषा और सॉफ्टवेयर का उपयोग करने का एक अन्य लाभ यह है कि यह स्थिर ग्राफ की सुविधा प्रदान करता है जो गुणवत्ता वाले ग्राफ के उत्पादन में सहायक होते हैं। कुछ अतिरिक्त पैकेज गतिशील और इंटरैक्टिव ग्राफिक्स के लिए उपयोग किए जाते हैं।

इस भाषा के सॉफ़्टवेयर में एक सामान्य सार्वजनिक लाइसेंस है, इसलिए इसकी उपलब्धता निःशुल्क है। R का कोड आमतौर पर उच्च-स्तरीय भाषाओं जैसे [C](/hi/programming/c/) और स्वयं R में भी लिखा जाता है। सॉफ़्टवेयर में RStudio और Jupyter (नोटबुक इंटरफ़ेस) के ग्राफ़िकल यूज़र इंटरफ़ेस जैसे तृतीय-पक्ष इंटरफ़ेस की उपलब्धता के साथ एक कमांड-लाइन इंटरफ़ेस शामिल है। R के पुस्तकालयों के कार्यान्वयन में उपयोग की जाने वाली सांख्यिकीय तकनीकें हैं। इसमें रेखीय और अरेखीय जैसे मॉडलिंग भी शामिल हैं।


## संक्षिप्त इतिहास ##

यह भाषा एस भाषा के साथ-साथ लेक्सिकल स्कूपिंग के सिमेंटिक्स का कार्यान्वयन है। 1976 में बेल लैब्स में, जॉन चेम्बर्स ने एस भाषा विकसित की। यहां तक कि आर भाषा में उपयोग किए जाने पर एस-प्लस के अधिकांश कोड में कोई बदलाव नहीं होता है। 1995 में, मार्टिन माक्लर और उनके साथियों ने आम जनता के लाइसेंस के तहत मुफ्त सॉफ्टवेयर के साथ आर भाषा बनाई।

व्यापक आर आर्काइव नेटवर्क की आधिकारिक घोषणा 23 अप्रैल 1997 को की गई थी। 2000 में संस्करण 1. 0, जो पहला स्थिर बीटा था, आधिकारिक तौर पर जारी किया गया था। इसका पहला विमोचन 1995 में हुआ, जबकि CRAN (व्यापक आर संग्रह नेटवर्क) बाद के वर्षों में जारी किया जा रहा था।

पहली रिलीज के बाद भाषा के आगे के विकास के लिए 1997 में एक कोर टीम बनाई गई थी। कई अद्यतन और संशोधित संस्करण बाद के वर्षों में जारी किए जा रहे थे और आधुनिक ऑपरेटिंग सिस्टम और प्रौद्योगिकी के अनुसार नई सुविधाओं को शामिल किया गया था। हालिया संशोधन को 2021 के मई में पेश किया गया था।


## तकनीकी विशिष्टता ##

R एक व्याख्या करने वाली भाषा है और इस भाषा तक पहुँचने के लिए एक कमांड-लाइन दुभाषिया की आवश्यकता होती है। योग जैसी गणना कमांड प्रोमो में टाइप की जाती है और व्याख्या के बाद परिणाम दिखाए जाते हैं। डेटा और कोड को एस-एक्सप्रेशन के माध्यम से दर्शाया जाता है। इस भाषा की एक और विशिष्टता यह है कि इसे एक टूलबॉक्स के रूप में संचालित किया जा सकता है जो सामान्य मैट्रिक्स गणना की सुविधा प्रदान करता है।

R कोड को चलाने और संपादित करने के लिए विभिन्न अनुप्रयोगों का उपयोग किया जाता है। आर प्रोग्रामिंग भाषा के कोड को चलाने के लिए रैटल जीयूआई, आरकेवार्ड जैसे एकीकृत विकास वातावरण भी उपलब्ध हैं। माइक्रोसॉफ्ट का एक अन्य सॉफ्टवेयर जिसे माइक्रोसॉफ्ट आर ओपन के नाम से जाना जाता है, मल्टीथ्रेडेड कंप्यूटेशंस जैसे जटिल कंप्यूटेशंस के लिए आर वितरण के साथ संगतता के साथ भी उपलब्ध है। आर दुनिया भर की पांच चयनित प्रोग्रामिंग भाषाओं में से एक है जिसमें अपाचे स्पार्क एपीआई शामिल है।

R भाषा कार्यों के साथ-साथ प्रक्रियात्मक प्रोग्रामिंग का समर्थन करती है। हालाँकि, विशेष रूप से कुछ कार्यों के लिए, यह सामान्य कार्यों के साथ-साथ OOP (ऑब्जेक्ट-ओरिएंटेड प्रोग्रामिंग) का समर्थन करता है। मानों का उपयोग तर्कों को पारित करने के लिए किया जाता है यदि फ़ंक्शन और उनका मूल्यांकन तब होता है जब उनका उपयोग किया जाता है, जिसका अर्थ है कि कार्यों को बुलाए जाने पर उनका मूल्यांकन नहीं किया जाता है।

## आर फाइल प्रारूप उदाहरण ##

### वाक्य - विन्यास ###

```{r}
> x <- 1:6 # Create a numeric vector in the current environment
> y <- x^2 # Create vector based on the values in x.
> print(y) # Print the vector’s contents.
[1]  1  4  9 16 25 36

> z <- x + y # Create a new vector that is the sum of x and y
> z # return the contents of z to the current environment.
[1]  2  6 12 20 30 42

> z_matrix <- matrix(z, nrow=3) # Create a new matrix that turns the vector z into a 3x2 matrix object
> z_matrix 
     [,1] [,2]
[1,]    2   20
[2,]    6   30
[3,]   12   42

> 2*t(z_matrix)-2 # Transpose the matrix, multiply every element by 2, subtract 2 from each element in the matrix, and return the results to the terminal.
     [,1] [,2] [,3]
[1,]    2   10   22
[2,]   38   58   82

> new_df <- data.frame(t(z_matrix), row.names=c('A','B')) # Create a new data.frame object that contains the data from a transposed z_matrix, with row names 'A' and 'B'
> names(new_df) <- c('X','Y','Z') # set the column names of new_df as X, Y, and Z.
> print(new_df)  #print the current results.
   X  Y  Z
A  2  6 12
B 20 30 42

> new_df$Z #output the Z column
[1] 12 42

> new_df$Z==new_df['Z'] && new_df[3]==new_df$Z # the data.frame column Z can be accessed using $Z, ['Z'], or [3] syntax, and the values are the same. 
[1] TRUE

> attributes(new_df) #print attributes information about the new_df object
$names
[1] "X" "Y" "Z"

$row.names
[1] "A" "B"

$class
[1] "data.frame"

> attributes(new_df)$row.names <- c('one','two') ## access and then change the row.names attribute; can also be done using rownames()
> new_df
     X  Y  Z
one  2  6 12
two 20 30 42
```

### समारोह ###

```{r}
# Declare function “f” with parameters “x”, “y“
# that returns a linear combination of x and y.
f <- function(x, y) {
  z <- 3 * x + 4 * y
  return(z) ## the return() function is optional here
}
```

```{r}
> f(1, 2)
[1] 11

> f(c(1,2,3), c(5,3,4))
[1] 23 18 25

> f(1:3, 4)
[1] 19 22 25
```

### मॉडलिंग की दिनांक

```{r}
> x <- 1:6 # Create x and y values
> y <- x^2  
> model <- lm(y ~ x)  # Linear regression model y = A + B * x.
> summary(model)  # Display an in-depth summary of the model.

Call:
lm(formula = y ~ x)

Residuals:
      1       2       3       4       5       6
 3.3333 -0.6667 -2.6667 -2.6667 -0.6667  3.3333

Coefficients:
            Estimate Std. Error t value Pr(>|t|)   
(Intercept)  -9.3333     2.8441  -3.282 0.030453 * 
x             7.0000     0.7303   9.585 0.000662 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 3.055 on 4 degrees of freedom
Multiple R-squared:  0.9583, Adjusted R-squared:  0.9478
F-statistic: 91.88 on 1 and 4 DF,  p-value: 0.000662

> par(mfrow = c(2, 2))  # Create a 2 by 2 layout for figures.
> plot(model)  # Output diagnostic plots of the model.
```

## संदर्भ ##

* [आर - विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/R_(programming_language))


