#  Bugs and Commands

## Part 1 - Bugs

I chose the reversed(int[] arr) method, here is the original implementation:
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
    }
```

Failure Inducing Test:
```
@Test
  public void testReversed1() {
    int[] input = { 0, 2, 4 };
    assertArrayEquals(new int[] { 4, 2, 0 }, ArrayExamples.reversed(input));
  }
```
Successful Test:
```
@Test
  public void testReversed2() {
    int[] input = {};
    assertArrayEquals(new int[] {}, ArrayExamples.reversed(input));
  }
```
The Symptom:
![Image](reversedTests.jpg)

The Bug:
<br/> The bug in reversed(int[] arr) is that it returns the original array arr instead of the new array newArray which is supposed to hold the elements of arr in reversed order.
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
    }
```
<br/>
<br/>

## Part 2 - Researching Commands ( less )

### -N or --LINE-NUMBERS
```
less -N  technical/911report/chapter-7.txt
      1 
      2     
      3         
      4             THE ATTACK LOOMS
      5             FIRST ARRIVALS IN CALIFORNIA
      6             In chapter 5 we described the Southeast Asia travels of Nawaf al Hazmi, Khalid al
      7                 Mihdhar, and others in January 2000 on the first part of the "planes operation." In
      8                 that chapter we also described how Mihdhar was spotted in Kuala Lumpur early in
      9                 January 2000, along with associates who were not identified, and then was lost to
     10                 sight when the group passed through Bangkok. On January 15, Hazmi and Mihdhar
     11                 arrived in Los Angeles. They spent about two weeks there before moving on to San
     12                     Diego.
     13             
     14             Two Weeks in Los Angeles
     15             Why Hazmi and Mihdhar came to California, we do not know for certain. Khalid Sheikh
     16                 Mohammed (KSM), the organizer of the planes operation, explains that California was
     17                 a convenient point of entry from Asia and had the added benefit of being far away
     18                 from the intended target area.
     19             
     20             Hazmi and Mihdhar were ill-prepared for a mission in the United States. Their only
     21                 qualifications for this plot were their devotion to Usama Bin Ladin, their veteran
     22                 service, and their ability to get valid U.S. visas. Neither had spent any
     23                 substantial time in the West, and neither spoke much, if any, English.
      ...
```
```
less -N technical/biomed/1468-6708-3-3.txt
      1 
      2   
      3     
      4       
      5         The problem
      6         Three published [ 1 2 3 ] and one recently presented [ 4
      7         ] randomized placebo-controlled clinical trial have
      8         unequivocally demonstrated that 3-Hydroxy-3-methylgluatryl
      9         coenzyme A (HMG CoA) reductase inhibitors (statins) reduce
     10         the morbidity and mortality associated with coronary
     11         disease. These trials found that when compared with
     12         placebo, statins significantly reduced the incidence of
     13         death, myocardial infarction, unstable angina, percutaneous
     14         and surgical coronary revascularization, and stroke in
     15         persons with 
     16         stable coronary disease. Because
     17         patients who had experienced an acute coronary syndrome
     18         within three to six months of enrollment were excluded,
     19         these trials did not assess the effect of lipid-lowering
     20         therapy on adverse cardiovascular events in those with
     21         recently 
     22         unstable coronary disease. Whether
     23         lipid-lowering therapy would provide incremental benefit if
     24         initiated immediately following an acute coronary syndrome
      ...
```
less -N shows numbers for each line, which is very useful for finding and talking about exact spots in files.


```
FIRST ARRIVALS IN ==CALIFORNIA==
            In chapter 5 we described the Southeast Asia travels of Nawaf al Hazmi, Khalid al
                Mihdhar, and others in January 2000 on the first part of the "planes operation." In
                that chapter we also described how Mihdhar was spotted in Kuala Lumpur early in
                January 2000, along with associates who were not identified, and then was lost to
                sight when the group passed through Bangkok. On January 15, Hazmi and Mihdhar
                arrived in Los Angeles. They spent about two weeks there before moving on to San
                    Diego.
            
            Two Weeks in Los Angeles
            Why Hazmi and Mihdhar came to ==California==, we do not know for certain. Khalid Sheikh
                Mohammed (KSM), the organizer of the planes operation, explains that ==California== was
                a convenient point of entry from Asia and had the added benefit of being far away
                from the intended target area.
            
            Hazmi and Mihdhar were ill-prepared for a mission in the United States. Their only
                qualifications for this plot were their devotion to Usama Bin Ladin, their veteran
                service, and their ability to get valid U.S. visas. Neither had spent any
                substantial time in the West, and neither spoke much, if any, English.
            
            It would therefore be plausible that they or KSM would have tried to identify, in
                advance, a friendly contact for them in the United States. In detention, KSM denies
                that al Qaeda had any agents in Southern ==California==. We do not credit this
                denial.4We believe it is unlikely that Hazmi and Mihdhar-neither of whom, in
                contrast to the Hamburg group, had any prior exposure to life in the West-would have
                come to the United States without arranging to receive assistance from one or more
                individuals informed in advance of their arrival.
```







