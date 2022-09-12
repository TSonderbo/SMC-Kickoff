# SMC-Kickoff

## Project Background

### Introduction
Noise can affect the listening experience when using headphones as it distracts from the audio coming from the headphone speakers.
Traffic is the main source of noise impact in Denmark. Traffic noise is present in most outdoor areas near roads and affects aproximately 1 in 3 houses (MST 2022). Some examples of sources of traffic are motorvehicles, trains & railways and airplanes.     
Active noise cancelation (ANC) can be used to reduce the percieved noise levels of traffic noise (Kang, Moon, Lim 2014). This involves using microphones to record noise from the environment and playing corresponding anti noise through speakers.      
Bang & Olufsen is a company that manufacturs headphones. They are interested in implementing ANC into their headphones. 

### Problem Statement
How can noise be removed from the listening environment to enhance the listening experience, without affecting the quality of the sound? 

### Definition of purpose
The purpose of this project is to design an ANC algorithm that can reduced percieved traffic noise in headphones.

### Delimitation
This project will not design acoustic noise reduction.   
This project will not design headphones.

## Methodology
This project will use SCRUM as a development methodology.

## Risk assessment
| Risk        | Likelihood  | Severity    | Product     | Mitigation  | Identifier | Responsible  |
| ----------- | ----------- | ----------- | ----------- | ----------- | ---------- | ------------ |
| Hardware provider fails to deliver      | 1           | 4           | 4           | Change provider      | Late delivery/No delivery |  Person 1 |
| Item 2      | 3           | 2           | 6           | Do thing    | Other thing happens | Person 2|
## Analysis

## Requirements
This section contains the requirements determined for the project. The requirements are ordered in order of importance using MoSCoW.
### Functional Requirements
* Must be able to filter noise traffic noise (Cars, Trains, Airplanes etc.)

* Must able to adjust filtered amount of background noise

* Must be able to adjust which types of audio to filter

* Must be able to enable and disable noise filtering

* Should be able to enable and disable microphones
### Non-Functional Requirements
* Must be able to record audio from user

* Must be able to run wirelessly over Bluetooth 5.1 

* Must have a visual indicator that the product is turned on 

* Must have a visual indicator that the product is filtering audio 

* Must be power efficient

* Should be able to play audio from multiple sources

* Could be controllable via a phone app

## Research
ANC can be done in two overall ways, either Adaptive or Active Noise cancelling. Both are ways to remove ambient noise. 
Adaptive NC predicts the incoming noise, where as Active is more stationary (Guldenschuh, Hördrich. 2013, p. 497)

The earcup of headphones dampens incoming frequencies, but due to the difference of low and high frequencies, they primarily dampen high frequencies. By introducing a high pass filter, it is possible  to equally dampen the low frequencies, and thus dampen the whole spectrum of sounds.
One way to do this is using a LMS algorithm (least mean squares) (Guldenschuh and Höldrich, 2013 p, 497).

Feedback ANC requires one microphone in each earcup, which analyses the incoming noise (x). The ADC (Analogue to digital converter)/DAC (Digital to analogue converter) creates a small amount of latency which can be minimised by using prediction of x. By focusing on the lower frequencies, the bandwith of the prediction are minimised, and thus can make a better prediction.
This form of ANC can minimize traffic and train noise (Guldenschuh and Höldrich, 2013 p, 497).

Another way implementing ANC is via phase cancelation, i.e. phase inverting the incoming signal and thus cancelling the sound. This is usually done by using an abundance of filters and microphones, where each circuit are focusing different bandwith of the sound spectrum. As this does not have earcups, this is usually the preferred method in inear and hearing aids.
e.g you could use 6 microphones and filters that focus on removing the human voice, which approximately are betweet 300-3000hz (Liu, et al, 2020, pp. 1-3).

By using both methods, both voice and traffic can be significantly reduced.

## Timetable
Timetable for the project is available as a Gantt chart in the root folder of the project.
## Sources of information
Miljøstyrrelsen - Traffic noise https://eng.mst.dk/air-noise-waste/noise/traffic-noise/     
Won-Pyoung Kang, Hak-Ryong Moon and You-Jin Lim - A Comparative Study Reducing Road Noise using Active Noise Cancelation    
Liu, H., Liu, S., Shkel, A. A., & Kim, E. S. (2020). Active noise cancellation with MEMS resonant microphone array. Journal of Microelectromechanical Systems, 29(5), 839-845.  
Guldenschuh, M., & Höldrich, R. (2013). Prediction filter design for active noise cancellation headphones. IET Signal Processing, 7(6), 497-504.