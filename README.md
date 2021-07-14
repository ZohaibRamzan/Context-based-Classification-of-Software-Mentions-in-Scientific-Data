# Contextual-based-Classification-of-Software-Mentions-in-Scientific-Data(Bio-medical & Life Sciences)

<h2>Motivation</h2>
<li>
To know about which software / framework that researchers mostly use in their work</li>
<li>About Software availability and attribution of software developer</li>

<h2>Objective</h2>
<ul>
<li>To classify the Software Mentions appearing in text data , extracted from Bio medical and Social
Sciences articles or research papers.</li>
<li>To provide basis for building SoftwareKG</li>
</ul>
<h2>Classifcation</h2>
There are four classes in which software mentions will be categorized as per their context.
<ol>
<li>Usage- If software is being actually used by the researcher</li>
<li>Mention- If software is just mentioned / disclosed / referred by the researcher but has not
actually used it.</li>
<li>Creation- If software is being developed by the researcher</li>
<li>Deposition-If software is being first created and then deposited it somewhere for future
availability by the researcher</li>
</ol>

<h2>Data Pre-processing</h2>
<ol>
  <li>Annotated Software mentions using Brat Annotation Tool</li>
  <ul>
    <li> 1,727 Files were annotated</li>
    <li>5,309 Sentences were annotated and extracted for Feature Space</li>
  </ul>
<li>Brat Standoff Format to BIO Encoded Format
<ul>
  <li>Relevant Sentence Extraction</li>
  <li>Sentence Tokenization</li>
  <li>BIO Encoding</li>
  </li>
</ol>

<h2>Feature Engineering</h2>
<ul>
  <li>Replace Software Mentions with place holder</li>
 <li>Extract Software Mentions Contextual Features
  <ul><li>Find out Software Mentions Position</li>
  <li>Extract Contextual Words as per window_size of 3</li>
    <li>Padding if needed</li></ul></li>
   
<li>Generate Word Embeddings of Contextual Words
<ul><li>Used Pre trained Model (wikipedia pubmed and PMC w2v.bin)
  </li></ul>
 <li>Generate Word Embeddings for POS tags of Contextual Words
  </li>
<li>Generate Specific Class based features
  <li>Frequent Words, Frequent tags etc.</li>
  </li>
<li>Features Concatenation</li>
</ul>
  

