---
title: Publications
permalink: /publication/
---

<head>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/pcooksey/bibtex-js/src/bibtex_js.js">

  <bibtex src="{{site.baseurl}}/references.bib"></bibtex>
</script>

</head>

<body>
<h1>{{page.title}}<h1>

<div class="container-fluid">
	<div class="searchbar">
		<div style="float:left;">
			<button type="button" class="btn btn-default" onclick="reset()">Reset</button>
		</div>
		<div style="float:left;">
			<select id="authorselectfirst" class="btn bibtex_search bibtex_author" style="border: 1px solid lightgrey;" extra="first" search="author">
			  <option value="">Search First Author</option>
			</select>
		</div>
		<div style="float:left;">
			<select id="authorselect" class="btn bibtex_search bibtex_author" style="border: 1px solid lightgrey;" search="author">
			  <option value="">Search Author</option>
			</select>
		</div>
		<div style="float:left;">
			<select id="topicselect" class="btn bibtex_search" style="border: 1px solid lightgrey;">
			  <option value="">Search Topic</option>
			  <!-- Add topic values here -->
			  <option value="Example topic">Example Topic</option>
			</select>
		</div>
		<div style="float:left;">
			<input type="text" class="bibtex_search form-control" id="searchbar" placeholder="Search publications">
			<span class="help-block">Example: journal 2015 (finds the intersection of the two terms)</span>
		</div>
	</div>
</div>

<div class="bibtex_structure">
  <div class="group year" extra="ASC number">
  	  <a href="#top" style="display: inline"><em>(Top of the page)</em></a>
  	  <div style="padding-bottom:10px;"></div>
  	  <div class="sort journal" extra="DESC string">
      	<div class="templates"></div>
      </div>
  </div>
</div>

<div id="bibtex_display">

  <div class="bibtex_template" style="display: none;">
    <ul> <li>
      <span class="if title">
        <a class="bibtexVar" href="http://www.website.com/~demo/papers/+BIBTEXKEY+.pdf" extra="BIBTEXKEY">
            <span style="text-decoration: underline;" class="title"></span>,
        </a>
      </span>
      <div class="if author">
        <span class="author"></span>
      </div>
      <div>
        <span class="if journal"><em><span class="journal"></span></em>,</span>
        <span class="if publisher"><em><span class="publisher"></span></em>,</span>
        <span class="if booktitle">In <em><span class="booktitle"></span></em>,</span>
        <span class="if address"><span class="address"></span>,</span>
        <span class="if month"><span class="month"></span>,</span>
        <span class="if year"><span class="year"></span>.</span>
        <span class="if note"><span class="note"></span></span>
        <a class="bibtexVar" role="button" data-toggle="collapse"
	   href="#bib+BIBTEXKEY+" aria-expanded="false"
	   aria-controls="bib+BIBTEXKEY+" extra="BIBTEXKEY" bibtexjs-css-escape>
		  [bib]
		</a>
      </div>
      <div class="bibtexVar collapse" id="bib+BIBTEXKEY+" extra="BIBTEXKEY">
		  <div class="well">
		    <pre><span class="bibtexraw noread"></span></pre>
		  </div>
	  </div>
	  <div style="display:none"><span class="bibtextype"></span></div>
    </li></ul>
  </div>

</div>

### Copyright Notice

The documents listed here are available for downloading and have been provided as a means to ensure timely dissemination of scholarly and technical work on a noncommercial basis. Copyright and all rights therein are maintained by the authors or by other copyright holders, notwithstanding that they have offered their works here electronically. It is understood that all persons copying this information will adhere to the terms and constraints invoked by each author's copyright. These works may not be re-posted without the explicit permission of the copyright holder.
