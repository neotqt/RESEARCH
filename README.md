# Research Proposal
Exploring the question: "Can AI technology capture musical significance the same way humans do?" I have defined "significance" metrics [such as rhythm stability and % of in-tune notes] using Python. I have built a classifier to label the generated pieces of music as significant or not significant. I am modifying an existing music generation model to create unique pieces of music that sound similar to files it has already listened to. The ultimate objective is to publish my work in a research journal or display my research at a conference.

Understanding how AI performs given different musical contexts can contribute to the 
development of AI systems that can assist or collaborate with human composers more
effectively. This knowledge can help musicians and composers leverage AI to enhance their 
creative processes. This question taps into the broader discussion of AI’s role in creative
processes. Does AI excel in certain aspects of music composition and how can it complement
human creativity?

The research can lead to the development of AI tools that assist composers and musicians in
creating more meaningful and emotionally resonant music. Composers can use AI  to explore
different musical contexts and styles, resulting in more versatile compositions. Furthermore, if this
problem can define where AI excels in music composition, any entertainment production can 
leverage this information to integrate AI-generated music to create dynamic soundtracks efficiently.

Current AI-generated music often struggles with producing creative and original compositions.
Understanding the impact of monophonic and polyphonic music can guide the development of AI 
systems that can generate more unique musical pieces. There is hardly depth and emotional 
expressiveness of human compositions. Investigating the meaningfulness of the generated 
compositions can lead to AI systems that better capture and convey emotions through music. 

## **Criteria Notebook Purpose and Introduction**

### **Purpose**
To clearly outline the three criteria that will be referenced throughout this paper.

### **Introduction**
Having predefined criteria allows for standardization in evaluating the quality and meaningfulness of music pieces in general. Below are the three criteria I have chosen.

**Criteria 1 ~ Tonality**: Tonality refers to the organization of pitches and harmonies around a central note, known as the tonic. In meaningful music, intentional tonality indicates a deliberate choice and adherence to a specific tonal center throughout the composition. This criterion assesses whether the music maintains a coherent tonal structure, such as major or minor keys, which can provide a sense of stability, direction, and emotional resonance to the listener.

**Criteria 2 ~ Meter**: Meter refers to the rhythmic framework or pulse that organizes musical patterns into regular beats or measures. In meaningful music, meter plays a crucial role in establishing rhythmic stability and providing a sense of groove or flow. This criterion evaluates whether the music maintains a consistent meter, such as 4/4 time or waltz time, and effectively utilizes rhythmic patterns to convey musical structure and coherence.

**Criteria 3 ~ Melodic Structure**: Melodic structure refers to how individual pitches are organized over time to form a coherent and memorable melody. It includes the shape of the melody (pitch contour), the distances between pitches (intervallic relationships), the rhythmic patterns, the division into musical phrases (phrasing), and the development of recurring motifs (motivic development).

## **Random Note Generation Notebook Purpose and Introduction**

### **Purpose**
To test the rigor of the three previously defined criteria.

### **Introduction**
By including pieces of music with random notes, I establish a baseline for comparison. These pieces lack intentional tonality, coherent meter, and meaningful melodic structure. Contrasting them with music that adheres to these criteria helps highlight the importance of intentional tonality, meter, and melodic structure in creating meaningful music.

## **CSV Creation Notebook Purpose and Introduction**

### **Purpose**
To create the Randomized Music Dataset, the Training Dataset, and the Testing Dataset which is then organized into a single CSV File.  

### **Introduction**
Combining all datasets into a single CSV file helps in organizing the data in a structured manner. This makes it easier to manage and maintain the datasets, reducing the risk of data duplication or inconsistency.

Splitting the dataset into training and testing sets is crucial for evaluating the performance of machine learning models. The training set is used to train the model, while the testing set is used to assess its performance on unseen data. This helps in estimating how well the model generalizes to new, unseen music samples.

## **Audio Classification Model Notebook Purpose and Introduction**

### **Purpose**
To create a classifier that can determine whether a piece is significant or insignificant [pieces that solely contain randomizations - a.k.a the randomMono.wav / randomPoly.wav files].

### **Introduction**
The classifier helps in assessing the quality and meaningfulness of generated music [at its most basic level]. It distinguishes between music pieces that exhibit intentional musical structure, such as tonality, meter, and melodic patterns, and those that consist solely of random notes.

## **Next Steps [in Progress]**

Currently, I am at the stage of creating a classifier that can determine whether a piece is significant or insignificant [pieces that solely contain randomizations - a.k.a the randomMono.wav / randomPoly.wav files].

However, I want to take this to the next level. I want to create / modify a model that can generate unique pieces, but similar-sounding music to files it has previously heard. My input would be the significant pieces I already have, and I want it to listen to those pieces, then create a unique, but similar sounding piece. I would then run a classifier determing whether that generated piece is significant or insignificant.

As of now, the classifier is trained to differentiate between "randomized" music and significant pieces of music. I think a more meaningful classification would be taking the different factors that determine significance [such as "'% In-Tune Notes', 'Rhythmic Stability', 'Note Distribution Stability', 'Melodic Stability Range', 'Dynamic Variation'"]. I believe this is a better approach for classifying the generated pieces, as I predict them to be "slightly significant." It would be hard to do binary classification on the piece as a whole, but easier for binary classification on the factors determining the significance of the piece.

Essentially, the there are two things I want to do: [1] Create a model that can generate unique, but similar sounding pieces based on previously heard pieces and [2] Modify my classification model to binary classify the different factors composing "significance" [such as "'% In-Tune Notes', 'Rhythmic Stability', 'Note Distribution Stability', 'Melodic Stability Range', 'Dynamic Variation'"] as significant or not rather than classify the piece as a whole [current implementation].
