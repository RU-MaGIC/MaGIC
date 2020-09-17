---
title: "Submit your project request"
permalink: /request/
---

<form id="fs-frm" name="survey-form" accept-charset="utf-8" action="https://formspree.io/YOUR_EMAIL_HERE" method="post">
  <fieldset id="fs-frm-inputs">
    <label for="full-name">Full Name</label>
    <input type="text" name="name" id="full-name" placeholder="First and Last" required="">
    <label for="email-address">Email Address</label>
    <input type="email" name="_replyto" id="email-address" placeholder="email@domain.tld" required="">
    <fieldset id="fs-frm-selects">
      <label for="project">Please select the type of project.</label>
      <select name="project" id="project" required="">
        <option value="Choose" selected="" disabled="">Choose Project Type</option>
        <option value="1">RNA-seq</option>
        <option value="2">scRNA-seq</option>
        <option value="3">Genome/Exome Sequencing</option>
        <option value="4">ATAC/ChIP Sequencing</option>
        <option value="5">Amplicon Sequencing</option>
        <option value="5">Other (please detail below)</option>
      </select>
      <label for="seq">Please select where the samples were sequenced.</label>
      <select name="seq" id="seq" required="">
        <option value="Choose" selected="" disabled="">Choose Sequencing Location</option>
        <option value="1">The Genomics Center at Rutgers NJMS</option>
        <option value="2">In my own lab</option>
        <option value="3">By a CRO or other outside lab</option>
        <option value="4">They havent been sequenced yet</option>
        <option value="4">They are from a data repository (please detail below)</option>
        <option value="5">Other (please detail below)</option>
      </select>
      <label for="consult">Do you need a consultation for your project before inception </label>
      <select name="project" id="project" required="">
        <option value="Choose" selected="" disabled="">Choose</option>
        <option value="1">Yes, please contact me immediately</option>
        <option value="2">No, please only contact me if you have questions</option>
      </select>
    </fieldset>
    <label for="message">Project Details</label>
    <textarea rows="5" name="message" id="message" placeholder="Please detail your project here" required=""></textarea>
     <label for="wishlist">Wishlist</label> 
     <textarea rows="2" name="wishlist" id="wishlist" placeholder="If you have any particular wishlist items for the analysis, please list them here" required=""></textarea>
    <p>
      All project requests will be reviewed within 1 business day. A member of MaGIC will contact you to confirm project request receipt and coordinate project details. 
      </p>  
    <input type="hidden" name="_subject" id="email-subject" value="Survey Responses">
  </fieldset>
  <input type="submit" value="Send Project Request">
</form>