<template>
  <el-carousel :interval="4000" type="card" height="300px">
    <el-carousel-item v-for="celebraty in celebraties" :key="celebraty.name">
      <el-image
        :src="require(`../assets/celebraties/${celebraty.portraitURL}`)"
        :fit="contain"
      />
      <div class="introduction">
        <p>{{ celebraty.name }}</p>
        <p>去世日期：{{ celebraty.deathDate }}</p>
        <p>生平简介：{{ celebraty.biography }}</p>
      </div>
    </el-carousel-item>
  </el-carousel>
</template>

<script>
export default {
  name: "CelebratyMemory",
  data() {
    return {
      celebraties: [
        {
          name: "袁隆平",
          deathDate: "2021-5-22",
          portraitURL: "ylp.jpg",
          biography:
            "袁隆平是我国研究与发展杂交水稻的开创者，也是世界上第一个成功地利用水稻杂种优势的科学家，被誉为“杂交水稻之父”。从1960年开始，他始终致力于杂交水稻技术的研究、应用与推广，发明“三系法”籼型杂交水稻，成功研究出“两系法”杂交水稻，创建了超级杂交稻技术体系，为我国粮食安全、农业科学发展和世界粮食供给作出杰出贡献。用一句话总结——让更多的人吃饱了饭",
        },
        {
          name: "鲁迅",
          deathDate: "1936-10-19",
          portraitURL: "lx.jpg",
          biography:
            "鲁迅是20世纪的文化巨人，他在小说、散文、杂文、木刻、现代诗、旧体诗、名著翻译、古籍校勘和现代学术等多个领域都有巨大贡献。鲁迅一生在文学创作、文学批评、思想研究、文学史研究、翻译、美术理论引进、基础科学介绍和古籍校勘与研究等多个领域具有重大贡献。他对于五四运动以后的中国社会思想文化发展具有重大影响，蜚声世界文坛，尤其在韩国、日本思想文化领域有极其重要的地位和影响，被誉为“二十世纪东亚文化地图上占最大领土的作家”",
        },
        {
          name: "周恩来",
          deathDate: "1976-1-8",
          portraitURL: "zel.jpg",
          biography:
            "周恩来（1898年3月5日-1976年1月8日） ，原籍浙江绍兴，1898年3月5日生于江苏淮安。1921年加入中国共产党，是伟大的马克思主义者，伟大的无产阶级革命家、政治家、军事家、外交家，党和国家主要领导人之一，中国人民解放军主要创建人之一，中华人民共和国的开国元勋，是以毛泽东同志为核心的党的第一代中央领导集体的重要成员。1976年1月8日在北京逝世。他的逝世受到极广泛的悼念。由于他一贯勤奋工作，严于律己，关心群众，被称为“人民的好总理”。他的主要著作收入《周恩来选集》。",
        },
        {
          name: "辛德勒",
          deathDate: "1974-10-9",
          portraitURL: "xdl.jpg",
          biography:
            "奥斯卡·辛德勒（德语：Oskar Schindler，1908年4月28日—1974年10月9日）是一位德国资本家、间谍和纳粹党党员，于第二次世界大战期间在现今位于波兰和捷克共和国境内的地区开设珐琅和弹药工厂，雇佣了许多犹太人作业，并最终成功挽救了1100名工人免遭德国纳粹的屠杀。1982年的小说《辛德勒的方舟》和1993年的电影《辛德勒的名单》都是以他为主题，反应了他起初作为一个投机主义者为了追求利润而在战争期间雇佣廉价工人开办工厂，但后来却展现出过人的胆识、主动性和坚韧的奉献精神，千方百计挽救犹太人生命的壮举。",
        },
      ],
    };
  },
};
</script>

<style scoped>
/* .el-carousel__item h3 {
  color: #475669;
  opacity: 0.75;
  line-height: 200px;
  margin: 0;
  text-align: center;
} */
.el-carousel__item {
  display: flex;
  font-size: 14px;
}
.introduction {
  width: 60%;
}
.el-carousel__item:nth-child(2n) {
  background-color: #d2a5e4;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d6c6db;
}
.el-carousel {
  position: absolute;
  top: 47%;
  left: 5%;
  width: 90%;
}
.el-image {
  height: 100%;
  width: 40%;
}
</style>
