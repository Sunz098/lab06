<script>
export default {
  data() {
    return {
      bec: {
        due_to: "",
        date: "",
        I_am: "",
        firstname: "",
        lastname: "",
        ID: "",
        Tel: "",
        Course: "",
        Group: "",
        Major: "",
        Transfer_to: "",
        Because: "",
      },
    };
  },
};
</script>

<template>
  <form action="" method="get">
    <div class="head">
      <h1>คำร้องขอเทียบโอนหน่วยกิต/ผลการเรียน</h1>
      <h2>สำหรับนักศึกษาที่พ้นสภาพการเป็นนักศึกษาจากมหาวิทยาลัยแม่โจ้</h2>
      <input
        type="radio"
        name="chooseone"
        id=""
        value="เนื่องจากลาออก"
        v-model="bec.due_to"
      />
      เนื่องจากลาออก
      <input
        type="radio"
        name="chooseone"
        id=""
        value="ขาดการติดต่อ"
        v-model="bec.due_to"
      />
      ขาดการติดต่อ
      <input
        type="radio"
        name="chooseone"
        id=""
        value="ผลการเรียนไม่ถึงเกณฑ์ที่กำหนด"
        v-model="bec.due_to"
      />
      ผลการเรียนไม่ถึงเกณฑ์ที่กำหนด
    </div>
    <input type="date" v-model="bec.date" />
    <p>เรื่อง ขอเทียบโอนหน่วยกิต / ผลการเรียน</p>
    <p>เรียน ผู้อำนวยการสำนักบริหารและพัฒนาวิชาการ</p>
    <div>
      ข้าพเจ้า
      <select name="selectprefix" v-model="bec.I_am">
        <option value="นาย">นาย</option>
        <option value="นาย">นาง</option>
        <option value="นาย">นางสาว</option>
      </select>
    </div>
    <div>
      <p>
        ชื่อ:
        <input name="firstname" type="text" maxlength="50" v-model="bec.firstname" />
        นามสกุล:
        <input name="lastname" type="text" maxlength="50" v-model="bec.lastname" />
      </p>
      <p>
        รหัสนักศึกษา (10หลัก) :
        <input name="stuid" type="number" maxlength="10" v-model="bec.ID" />
      </p>
      <p>
        โทรศัพท์มือถือ (10หลัก) :
        <input type="tel" name="tele" maxlength="10" v-model="bec.Tel" />
      </p>
      <p>
        หลักสูตร
        <select name="selectcourse" v-model="bec.Course">
          <option value="4-5ปี">4-5ปี</option>
          <option value="4ปีเทียบเข้าเรียน">4ปีเทียบเข้าเรียน</option>
          <option value="บัณฑิตศึกษา">บัณฑิตศึกษา</option>
          <option value="ภาคปกติ">ภาคปกติ</option>
          <option value="ภาคสมทบ">ภาคสมทบ</option>
        </select>
      </p>
      <p>
        คณะ :
        <select name="selectgrop" v-model="bec.Group">
          <option value="คณะผลิตกรรมการเกษตร">คณะผลิตกรรมการเกษตร</option>
          <option value="คณะบริหารธุรกิจ">คณะบริหารธุรกิจ</option>
          <option value="คณะวิทยาศาสตร์">คณะวิทยาศาสตร์</option>
          <option value="คณะศิลปศาสตร์">คณะศิลปศาสตร์</option>
          <option value="คณะสถาปัตยกรรมศาสตร์ และการออกแบบสิ่งแวดล้อม ">
            คณะสถาปัตยกรรมศาสตร์ และการออกแบบสิ่งแวดล้อม
          </option>
          <option value="คณะเทคโนโลยีการประมง และทรัพยากรทางน้ำ">
            คณะเทคโนโลยีการประมง และทรัพยากรทางน้ำ
          </option>
          <option value="คณะวิศวกรรมและอุตสาหกรรมเกษตร ">
            คณะวิศวกรรมและอุตสาหกรรมเกษตร
          </option>
          <option value="คณะพัฒนาการท่องเที่ยว ">คณะพัฒนาการท่องเที่ยว</option>
          <option value="คณะเศรษฐศาสตร์ ">คณะเศรษฐศาสตร์</option>
          <option value="วิทยาลัยบริหารศาสตร์ ">วิทยาลัยบริหารศาสตร์</option>
          <option value="วิทยาลัยพลังงานทดแทน ">วิทยาลัยพลังงานทดแทน</option>
          <option value="วิทยาลัยนานาชาติ ">วิทยาลัยนานาชาติ</option>
          <option value="มหาวิทยาลัยแม่โจ้-แพร่ เฉลิมพระเกียรติ ">
            มหาวิทยาลัยแม่โจ้-แพร่ เฉลิมพระเกียรติ
          </option>
          <option value="มหาวิทยาลัยแม่โจ้-ชุมพร ">มหาวิทยาลัยแม่โจ้-ชุมพร</option>
          <option value="คณะพยาบาลศาสตร์">คณะพยาบาลศาสตร์</option>
          <option value="คณะสัตวแพทย์ศาสตร์">คณะสัตวแพทย์ศาสตร์</option>
        </select>
        สาขา
        <select name="selectbranch" id="" v-model="bec.Major">
          <option value="เกษตรศาสตร์">เกษตรศาสตร์</option>
          <option value="พืชสวน">พืชสวน</option>
          <option value="เทคโนโลยีอาหาร">เทคโนโลยีอาหาร</option>
          <option value="เทคโนโลยีอุสาหการ การผลิต">เทคโนโลยีอุสาหการ การผลิต</option>
          <option value="เทคโนโลยีพอลิเมอร์">เทคโนโลยีพอลิเมอร์</option>
          <option value="วิศวกรรมเกษตร">วิศวกรรมเกษตร</option>
          <option value="วิศวกรรมอาหาร">วิศวกรรมอาหาร</option>
          <option value="คณิตศาสตร์">คณิตศาสตร์</option>
          <option value="เคมี">เคมี</option>
          <option value="เทคโนโลยีชีวภาพ">เทคโนโลยีชีวภาพ</option>
          <option value="ฟิสิกส์">ฟิสิกส์</option>
          <option value="วัสดุศาสตรฺ">วัสดุศาสตรฺ</option>
          <option value="สถิติ">สถิติ</option>
          <option value="เทคโนโลยีสารสนเทศ">เทคโนโลยีสารสนเทศ</option>
          <option value="วิทยาการคอมพิวเตอร์">วิทยาการคอมพิวเตอร์</option>
          <option value="รัฐประศาสนศาสตร์">รัฐประศาสนศาสตร์</option>
          <option value="รัฐศาสตร์">รัฐศาสตร์</option>
          <option value="การเงิน">การเงิน</option>
          <option value="การจัดการ">การจัดการ</option>
          <option value="การบัญชี">การบัญชี</option>
          <option value="การตลาด">การตลาด</option>
          <option value="ระบบสารสนเทศ">ระบบสารสนเทศ</option>
          <option value="การท่องเที่ยวและการโรงแรม">การท่องเที่ยวและการโรงแรม</option>
          <option value="ประมง">ประมง</option>
          <option value="เศรษฐศาสตร์">เศรษฐศาสตร์</option>
          <option value="นิเทศศาสตร์">นิเทศศาสตร์</option>
          <option value="อังกฤษ">อังกฤษ</option>
          <option value="วิศวกรรมพลังงาน">วิศวกรรมพลังงาน</option>
          <option value="ดิจิทัล">ดิจิทัล</option>
          <option value="ภูมิสถาปัตยกรรม">ภูมิสถาปัตยกรรม</option>
          <option value="วางแผนภาคและเมือง">วางแผนภาคและเมือง</option>
          <option value="สถาปัตยกรรม">สถาปัตยกรรม</option>
          <option value="สัตวศาสตร์">สัตวศาสตร์</option>
          <option value="วนศาสตร์">วนศาสตร์</option>
          <option value="สังคมศาสตร์และพฤติกรรมศาสตร์">
            สังคมศาสตร์และพฤติกรรมศาสตร์
          </option>
          <option value="การปกครอง">การปกครอง</option>
        </select>
      </p>
      <p>
        มีความประสงค์จะขอโอนย้ายไปสาขาวิชา
        <select name="selectbranch2" id="" v-model="bec.Transfer_to">
          <option value="เกษตรศาสตร์">เกษตรศาสตร์</option>
          <option value="พืชสวน">พืชสวน</option>
          <option value="เทคโนโลยีอาหาร">เทคโนโลยีอาหาร</option>
          <option value="เทคโนโลยีอุสาหการ การผลิต">เทคโนโลยีอุสาหการ การผลิต</option>
          <option value="เทคโนโลยีพอลิเมอร์">เทคโนโลยีพอลิเมอร์</option>
          <option value="วิศวกรรมเกษตร">วิศวกรรมเกษตร</option>
          <option value="วิศวกรรมอาหาร">วิศวกรรมอาหาร</option>
          <option value="คณิตศาสตร์">คณิตศาสตร์</option>
          <option value="เคมี">เคมี</option>
          <option value="เทคโนโลยีชีวภาพ">เทคโนโลยีชีวภาพ</option>
          <option value="ฟิสิกส์">ฟิสิกส์</option>
          <option value="วัสดุศาสตรฺ">วัสดุศาสตรฺ</option>
          <option value="สถิติ">สถิติ</option>
          <option value="เทคโนโลยีสารสนเทศ">เทคโนโลยีสารสนเทศ</option>
          <option value="วิทยาการคอมพิวเตอร์">วิทยาการคอมพิวเตอร์</option>
          <option value="รัฐประศาสนศาสตร์">รัฐประศาสนศาสตร์</option>
          <option value="รัฐศาสตร์">รัฐศาสตร์</option>
          <option value="การเงิน">การเงิน</option>
          <option value="การจัดการ">การจัดการ</option>
          <option value="การบัญชี">การบัญชี</option>
          <option value="การตลาด">การตลาด</option>
          <option value="ระบบสารสนเทศ">ระบบสารสนเทศ</option>
          <option value="การท่องเที่ยวและการโรงแรม">การท่องเที่ยวและการโรงแรม</option>
          <option value="ประมง">ประมง</option>
          <option value="เศรษฐศาสตร์">เศรษฐศาสตร์</option>
          <option value="นิเทศศาสตร์">นิเทศศาสตร์</option>
          <option value="อังกฤษ">อังกฤษ</option>
          <option value="วิศวกรรมพลังงาน">วิศวกรรมพลังงาน</option>
          <option value="ดิจิทัล">ดิจิทัล</option>
          <option value="ภูมิสถาปัตยกรรม">ภูมิสถาปัตยกรรม</option>
          <option value="วางแผนภาคและเมือง">วางแผนภาคและเมือง</option>
          <option value="สถาปัตยกรรม">สถาปัตยกรรม</option>
          <option value="สัตวศาสตร์">สัตวศาสตร์</option>
          <option value="วนศาสตร์">วนศาสตร์</option>
          <option value="สังคมศาสตร์และพฤติกรรมศาสตร์">
            สังคมศาสตร์และพฤติกรรมศาสตร์
          </option>
          <option value="การปกครอง">การปกครอง</option>
        </select>
        <br />
        เนื่องจาก
        <br />
        <input name="why" type="text" size="100" v-model="bec.Because" />
      </p>
    </div>
  </form>

  <h3>{{ bec }}</h3>

</template> 

<style >
  h3{
    color: white; 
   
  }
</style>
