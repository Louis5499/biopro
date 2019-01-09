<template>
  <div class="text-area">
    <p class="self"><b>Nitish V. Thakor</b> is a Professor of Electrical and Computer Engineering and Biomedical Engineering at Johns
    Hopkins University since 1983. He has also been the Professor of Biomedical Engineering and served as the
    Director of Singapore Institute for Neurotechnology at the National University of Singapore since 2012. Prof.
    Thakor’s technical expertise is in the field of Neuroengineering, where he has pioneered many technologies for
    brain monitoring to prosthetic arms and neuroprosthesis. He has published over 380 refereed journal papers
    (Google H-Index 73, &gt;24,000 citations). He has also more than 20 patents issued or pending and co-founded
    3 active companies. He is currently the Editor in Chief of Medical and Biological Engineering and Computing,
    and was the Editor in Chief of IEEE TNSRE from 2005-2011. Prof. Thakor is a recipient of a Research Career
    Development Award from the National Institutes of Health and a Presidential Young Investigator Award from
    the National Science Foundation, and is a Fellow of the American Institute of Medical and Biological
    Engineering, Life Fellow of IEEE, Founding Fellow of the Biomedical Engineering Society, and Fellow of
    International Federation of Medical and Biological Engineering. He is a recipient of the award of the Academic
    Career Award and Technical Excellence in Neuroengineering from IEEE Engineering in Medicine and Biology
    Society, Distinguished Alumnus Award from Indian Institute of Technology, Bombay, India, and a Centennial
    Medal from the University of Wisconsin School of Engineering.</p>
    <h3>EXPERIENCE</h3>
    <div class="experience">
      <div><p>1974-1976 Electronics Engineer</p><p class="second">Philips Company (India)</p></div>
      <div><p>1977-1981	Teaching & Research Asst.</p><p class="second">University of Wisconsin, Madison</p></div>
      <div><p>1981-1983	Assistant Professor</p><p class="second">Northwestern University, Evanston Electrical Eng. & Computer Science</p></div>
      <div><p>1984-1986	Assistant Professor</p><p class="second">The Johns Hopkins University Biomedical Engineering School of Medicine</p></div>
      <div><p>1987-1994	Associate Professor</p><p class="second">The Johns Hopkins University Biomedical Engineering School of Medicine</p></div>
      <div><p>1994-present	Professor</p><p class="second">The Johns Hopkins University Biomedical Engineering School of Medicine</p></div>
      <div><p>2012-present	Professor</p><p class="second">National University of Singapore Professor, Biomedical Engineering</p></div>
    </div>
    <h3>AWARDS</h3>
    <div class="award">
      <ul>
        <li>National Scholarship, India; Graduate Fellowships, University of Wisconsin, Madison</li>
        <li>2nd Prize, Student Paper Competition, Annu. Conf. Eng. Med. Biol. (1981)</li>
        <li>1st Prize, Paper Competition, Symp. Computer Appl. Med. Care (1982)</li>
        <li>Research Career Development Award, The National Institutes of Health (1985-1990)</li>
        <li>The Presidential Young Investigator Award, The National Science Foundation (1985-1991)</li>
        <li>The Fulbright Fellowship, Cybernetics Institute, Barcelona, Spain, 1987.</li>
        <li>Centennial Achievement Medal - University of Wisconsin, School of Engineering, 1993.</li>
        <li>Fellow, American Institute of Medical and Biological Engineering, 1996; Fellow, Institute of Electrical and Electronics Engineers (IEEE) 1997, Founding Fellow, Biomedical Engineering Society, 2005.</li>
        <li>Distinguished Service Award, Indian Institute of Technology, Bombay, India, 2008 and Distinguished Alumnus Award, Indian Institute of Technology, Bombay, India, 2010.</li>
        <li>Technical Achievement Award from IEEE Engineering in Medicine and Biology Society, 2010.</li>
        <li>Distinguished Achievement Award, University of Wisconsin, School of Engineering, Madison, WI, 2010.</li>
        <li>Fellow, International Federation of Medical and Biological Engineering, 2012.</li>
        <li>Editor in Chief, IEEE Transactions on Neural Systems and Rehabilitation Engineering (2005-2011) and Medical and Biological Engineering and Computing (2013-present).</li>
        <li>Engineering Leadership Award, National University of Singapore, 2016.</li>
        <li>IEEE Engineering in Medicine and Biology Society, Academic Career Leadership Award, 2017</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  
}
</script>

<style lang="scss" scoped>
.text-area {
  width: 80%;
  .self {
    line-height: 26px;
  }
  .experience {
    div {
      display: flex;
      flex-direction: row;
      position: relative;
      width: 90%;
      margin: 5px 0;
      .second {
        position: absolute;
        left: 60%;
        width: 50%;
      }
    }
  }
  .award {
    ul {
      li {
        margin: 6px 0;
      }
    }
  }
  h3 {
    font-size: 2em;
  }
}
</style>
