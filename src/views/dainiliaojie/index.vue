<template>
  <div class="details">
    <!-- <Headerlun /> -->
    <div class="lun_warp">
      <div class="lun_con">
        <img src="@/assets/img/航空内部席位/内部席位.png" alt="" />
      </div>
    </div>
    <page />
    <div class="requirement">
      <div class="requ">
        <div class="requ-top">
          <span>带你了解航空专业的内部席位</span>
          <br>
          <span>总有一个适合你</span>
          <div class="circular"></div>
          <p>REQUIREMENTS</p>
        </div>
        <div class="img">
         <img src="@/assets/img/航空内部席位/大航空内部席位.png" alt="" />
        </div>
        <div class="number">
          <div class="left">
            <img src="@/assets/img/公共/航空专业详情页_03.png" alt="" />
          </div>
          <div class="right">
            <span class="orange">机长：</span>
            <span
              >民用航空器运输机长（以下简称机长）在飞行中最高的法律地位和至高无上的权力，航空活动中机长对航空器和旅客的安全负有直接的也是最终的责任。
我国《民用航空运输机长职责》中规定机长是依据中国民用航空规章取得航线运输驾驶员执照，并被航空运输企业聘为机长的飞行员，并明确了机长的十二条职责。
</span
            >
          </div>
        </div>
        <div class="number">
          <div class="left">
            <img src="@/assets/img/公共/航空专业详情页_06.png" alt="" />
          </div>
          <div class="right">
            <span class="blue">地勤：</span>
            <span
              >机场地勤为自有航空运输服务以及各大航空站（机场）建设营运以来，出现在各级民用、军用航空站的一项重要附加服务，和航空站的运作息息相关且不可或缺。</span
            >
          </div>
        </div>
        <div class="number">
          <div class="left">
            <img src="@/assets/img/公共/航空专业详情页_03_08.png" alt="" />
          </div>
          <div class="right">
            <span class="green">空姐：</span>
            <span
              >空姐，即女空中乘务员，泛指民航客机上从事旅客服务的女性工作人员，年龄一般在20-50岁，身高1.63-1.75米，要求端庄、秀丽，面容姣好，具有空中服务方面的专业修养。
主要职责是在民航飞机上确保乘客旅途中的安全和舒适（例如为乘客供应飞机餐等餐饮），指导乘客使用机上安全设备以及在紧急情况下组织乘客逃离飞机等等。飞机客舱服务是民航运输服务的重要组成部分，它直接反映了航空公司的服务质量。
</span
            >
          </div>
        </div>
         <div class="number">
          <div class="left">
            <img src="@/assets/img/公共/航空专业详情页_10.png" alt="" />
          </div>
          <div class="right">
            <span class="pink">签派员：</span>
            <span
              >签派员(DISPATCHER)是一个航空公司不可或缺的人员。他们的主要工作是搜集飞行信息、制定并申请飞行计划，与机长共同放行每个航班。属于非常重要的工种，可以根据情况推迟、调配甚至取消航班。</span
            >
          </div>
        </div>
         <div class="number">
          <div class="left">
            <img src="@/assets/img/公共/航空专业内部席位_03.jpg" alt="" />
          </div>
          <div class="right">
            <span class="hui">机务：</span>
            <span
              >航空机务，也就是（飞机检修），保障航空机务系统飞行安全，机械、航电设备等原因飞行事故万时率控制在0.1以下，飞机完好率始终保持在80%以上。维修质量高、保障能力强的安全技术人员。</span
            >
          </div>
        </div>
      </div>
    </div>

    <div class="inline">
      <div class="read-top">
        <img src="@/assets/img/shouye/航空专业内部席位_07.jpg" alt="" />
      </div>
      <div class="aviation_text">
        <div class="aviation_text_content">
          <a-form-model
            ref="ruleForm"
            :model="form"
            :rules="rules"
            :label-col="labelCol"
            :wrapper-col="wrapperCol"
          >
            <a-form-model-item ref="names" label="" prop="names">
              <div class="aviation_text_input">
                <span class="span"><em>*</em>学生姓名</span>
                <a-input
                  v-model="form.names"
                  placeholder="请填写姓名"
                  @blur="
                    () => {
                      $refs.names.onFieldBlur();
                    }
                  "
                ></a-input>
              </div>
            </a-form-model-item>
            <a-form-model-item ref="numbers" label="" prop="numbers">
              <div class="aviation_text_input">
                <span class="span"><em>*</em>手机号码</span>
                <a-input
                  v-model="form.numbers"
                  placeholder="请填写手机号码"
                  @blur="
                    () => {
                      $refs.numbers.onFieldBlur();
                    }
                  "
                ></a-input>
              </div>
            </a-form-model-item>
            <a-form-model-item ref="dates" label="" required prop="dates">
              <div class="aviation_text_input">
                <span class="span"><em>*</em>出生年月</span>
                <a-date-picker
                  v-model="form.dates"
                  type="date"
                  style="height: 0.35rem; color: #000 !important"
                  :size="size"
                  placeholder="请选择出生年月"
                  @blur="
                    () => {
                      $refs.dates.onFieldBlur();
                    }
                  "
                />
              </div>
            </a-form-model-item>

            <a-form-model-item
              ref="regions"
              label=""
              style="margin: 0"
              prop="regions"
            >
              <div class="aviation_text_cascader">
                <span class="span"><em>*</em>所选课程</span>
                <div class="from_three">
                  <a-select
                    v-model="form.regions"
                    placeholder="请选择课程"
                    @blur="
                      () => {
                        $refs.regions.onFieldBlur();
                      }
                    "
                    style="
                      width: 2rem;
                      font-size: 0.15rem;
                      height: 0.35rem;
                      color: #ccc;
                      overflow: hidden;
                    "
                  >
                    <a-icon
                      slot="suffixIcon"
                      type="caret-down"
                      style="width: 0.11rem; height: 0.08rem; color: #000"
                    />
                    <a-select-option value="清华大学">
                      <span style="color: #000">javaScript精选课程</span>
                    </a-select-option>
                    <a-select-option value="北大大学">
                      <span style="color: #000">jquery精选课程</span>
                    </a-select-option>
                  </a-select>
                </div>
              </div>
            </a-form-model-item>

            <a-form-model-item
              ref="educations"
              label=""
              style="margin: 0"
              prop="educations"
            >
              <div class="aviation_text_cascader">
                <span class="span"><em>*</em>当前学历</span>
                <div class="from_three">
                  <a-select
                    v-model="form.educations"
                    placeholder="请选择学历"
                    @blur="
                      () => {
                        $refs.educations.onFieldBlur();
                      }
                    "
                    style="
                      width: 2rem;
                      font-size: 0.15rem;
                      height: 0.35rem;
                      color: #ccc;
                      overflow: hidden;
                    "
                  >
                    <a-icon
                      slot="suffixIcon"
                      type="caret-down"
                      style="width: 0.11rem; height: 0.08rem; color: #000"
                    />
                    <a-select-option value="清华大学">
                      <span style="color: #000">大专学历</span>
                    </a-select-option>
                    <a-select-option value="北大大学">
                      <span style="color: #000">本科学历</span>
                    </a-select-option>
                  </a-select>
                </div>
              </div>
            </a-form-model-item>

            <a-form-model-item ref="id_numbers" label="" prop="id_numbers">
              <div class="aviation_text_input">
                <span class="span"><em>*</em>身份证号</span>
                <a-input
                  v-model="form.id_numbers"
                  placeholder="请填写身份证号"
                  @blur="
                    () => {
                      $refs.id_numbers.onFieldBlur();
                    }
                  "
                ></a-input>
              </div>
            </a-form-model-item>

            <a-form-model-item label="" prop="descs">
              <div class="aviation_textarea">
                <span>您的疑问</span>
                <div class="aviation_textarea_text">
                  <textarea
                    v-model="form.descs"
                    name=""
                    id=""
                    cols="30"
                    rows="10"
                    style="color: #000"
                    placeholder="请填写您的疑问"
                  >
                  </textarea>
                </div>
              </div>
            </a-form-model-item>
            <a-form-model-item :wrapper-col="{ span: 14, offset: 4 }">
              <!-- <a-button type="primary" @click="onSubmit"> -->
              <div class="bottom_jick">
                <div class="aviation_text_button" @click="onSubmit">
                  <span>立即提交</span>
                </div>
                <div class="submit-size">
                  <div>
                    <span @click="showModal">《隐私保障》</span>
                  </div>
                  <a-modal
                    v-model="visible"
                    title="隐私保障"
                    ok-text="确认"
                    cancel-text="取消"
                    @ok="hideModal"
                  >
                    <p>Bla bla ...</p>
                    <p>Bla bla ...</p>
                    <p>Bla bla ...</p>
                  </a-modal>
                  <br />
                  <br />
                </div>
              </div>
            </a-form-model-item>
          </a-form-model>
        </div>
      </div>
    </div>

    <div class="cdsa">
      <aviation />
    </div>
    <div class="read">
      <div class="read-top">
        <img src="@/assets/img/航空专业/推荐阅读_03.jpg" alt="" />
      </div>
      <div class="data">
        <div class="data-cont">
          <div class="left">
            <p>27</p>
            <p>2021.10</p>
          </div>
          <div class="right">
            <p>航空学校招生要求有哪些？</p>
            <p>空乘专业本科院校招生对高考成绩要求很高...</p>
          </div>
        </div>
        <div class="data-cont">
          <div class="left">
            <p>14</p>
            <p>2021.10</p>
          </div>
          <div class="right">
            <p>航空学校学费一年多少钱？</p>
            <p>海南空中乘务专业招生院校，海南空姐学校...</p>
          </div>
        </div>
        <div class="data-cont">
          <div class="left">
            <p>18</p>
            <p>2021.10</p>
          </div>
          <div class="right">
            <p>河北空乘职业学校有哪些？</p>
            <p>随着航空专业的热度，其他航空专业方向...</p>
          </div>
        </div>
        <div class="data-cont">
          <div class="left">
            <p>05</p>
            <p>2021.10</p>
          </div>
          <div class="right">
            <p>航空物流专业好就业吗？</p>
            <p>市北言咨,市民留言咨询这些问题,官...</p>
          </div>
        </div>
        <div class="data-cont">
          <div class="left">
            <p>21</p>
            <p>2021.10</p>
          </div>
          <div class="right">
            <p>空姐就业前景怎么样？</p>
            <p>随着航空服务专业学校的增多，所开设的专...</p>
          </div>
        </div>
        <div class="data-cont">
          <div class="left">
            <p>14</p>
            <p>2021.10</p>
          </div>
          <div class="right">
            <p>航空学校学费一年多少钱？</p>
            <p>海南空中乘务专业招生院校，海南空姐学校...</p>
          </div>
        </div>
        <div class="data-cont">
          <div class="left">
            <p>18</p>
            <p>2021.10</p>
          </div>
          <div class="right">
            <p>河北空乘职业学校有哪些？</p>
            <p>随着航空专业的热度，其他航空专业方向...</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Data from "@/views/details/data.vue";
import Headerlun from "@/components/header-lun/header_lun.vue";
import Aviation from "@/views/homes/major/aviation.vue";
import Five from "@/views/homes/Five/index.vue";
import Page from "@/components/page/index.vue";

export default {
  components: { Data, Headerlun, Aviation, Page },
  data() {
    return {
      visible: false,
      size: "default",
      labelCol: { span: 4 },
      wrapperCol: { span: 14 },
      other: "",
      form: {
        names: "",
        numbers: "",
        regions: undefined,
        dates: undefined,
        educations: undefined,
        id_numbers: undefined,
        descs: "",
      },
       rules: {
        names: [
          {
            required: true,
            message: "请填写姓名",
            trigger: "blur",
          },
          {
            pattern:/^[\u4E00-\u9FA5]{2,4}$/,
            message: "请填写正确的姓名",
            trigger: "blur",
          },
        ],
        numbers: [
          {
            required: true,
            message: "请填写手机号",
            trigger: "blur",
          },
          {
            pattern:/^[1][3,4,5,7,8][0-9]{9}$/,
            message: "请填写正确的手机号",
            trigger: "blur",
          },
        ],
        regions: [
          {
            required: true,
            message: "请选择课程",
            trigger: "blur",
          },
          {
            min: 3,
            max: 5,
            message: "请选择课程",
            trigger: "blur",
          },
        ],
        dates: [
          {
            required: true,
            message: "请选择出生年月",
            trigger: "change",
          },
        ],
        educations: [
          {
            required: true,
            message: "请选择学历",
            trigger: "blur",
          },
          {
            min: 3,
            max: 5,
            message: "请选择学历",
            trigger: "blur",
          },
        ],
        id_numbers: [
          {
            required: true,
            message: "请填写身份证号",
            trigger: "blur",
          },
          {
            pattern:/^[1-9][0-9]{5}(19|20)[0-9]{2}((01|03|05|07|08|10|12)(0[1-9]|[1-2][0-9]|30|31)|(04|06|09|11)(0[1-9]|[1-2][0-9]|30)|02(0[1-9]|[1-2][0-9]))[0-9]{3}([0-9]|x|X)$/,
            message: "请填写正确的身份证号",
            trigger: "blur",
          },
        ],
        descs: [
          {
            required: true,
            message: "请输入您的疑问",
            trigger: "change",
          },

        ],
      },
    };
  },
  methods: {
    onSubmit() {
      this.$refs.ruleForm.validate((valid) => {
        if (valid) {
          alert("submit!");
          console.log(this.form);
        } else {
          console.log("error submit!!");
          return false;
        }
      });
    },
    resetForm() {
      this.$refs.ruleForm.resetFields();
    },
    submit() {
      console.log(this.value);
    },
    showModal() {
      this.visible = true;
    },
    hideModal() {
      this.visible = false;
    },
    confirm() {
      this.$confirm({
        title: "Confirm",
        content: "Bla bla ...",
        okText: "确认",
        cancelText: "取消",
      });
    },
  },
};
</script>

<style lang='scss' scoped>
.lun_warp {
  width: 100%;
  height: 1.5rem;
  .lun_con {
    width: 3.75rem;
    height: 1.5rem;
    margin: 0 auto;
    img {
      width: 100%;
      height: 100%;
    }
  }
}
.title_warp {
  width: 100%;
  padding: 0 0.2rem;
  margin: 0.15rem 0;
  box-sizing: border-box;
  p {
    width: 100%;
    text-align: left;
    span {
      font-size: 0.14rem;
      font-weight: normal;
      font-stretch: normal;
      line-height: 0.07rem;
      letter-spacing: 0px;
      color: #888888;
    }
    .hang {
      margin-left: 0.05rem;
      font-family: PingFang-SC-Medium;
      font-size: 0.14rem;
      font-weight: normal;
      letter-spacing: 0px;
      color: #b0b0b0;
    }
  }
}
.requirement {
  width: 100%;
  // padding: 0.15rem 0.1rem;
  padding: 0 0.1rem 0.15rem 0.1rem;
  box-sizing: border-box;
  .requ {
    width: 100%;
    background: #fff;
    border-radius: 5px;
    overflow: hidden;
    .requ-top {
      width: 100%;
      padding: 0.2rem 0;
      font-size: 0.18rem;
      font-weight: 700;
      text-align: center;
      box-sizing: border-box;
      span{
        color: #000;
      }
      .circular {
        width: 0.04rem;
        height: 0.04rem;
        border-radius: 50px;
        background: rgb(102, 102, 102);
        margin: 0.05rem auto;
        position: relative;
      }
      .circular::before {
        content: "";
        position: absolute;
        display: block;
        right: 0.07rem;
        width: 0.5rem;
        top: 0.013rem;
        border-bottom: 1px solid rgb(102, 102, 102);
      }
      .circular::after {
        content: "";
        position: absolute;
        display: block;
        left: 0.07rem;
        width: 0.5rem;
        top: 0.013rem;
        border-bottom: 1px solid rgb(102, 102, 102);
      }
      p {
        font-size: 0.16rem;
        color: rgb(102, 102, 102);
      }
    }
    .img {
      width: 100%;
      height: 1.45rem;
      img {
        width: 100%;
        height: 100%;
      }
    }
    
    .number {
      width: 3.14rem;
      margin: 0.15rem 0.1rem;
      padding-bottom: 0.15rem;
      border-bottom: 1px dotted rgb(153, 153, 153);
      overflow: hidden;
      .left {
        float: left;
        width: 0.51rem;
        img {
          width: 100%;
          height: 0.53rem;
        }
      }
      .right {
        width: 2.53rem;
        float: left;
        font-size: 0.12rem;
        .orange {
          color: rgb(255, 51, 0);
        }
        .blue {
          color: rgb(0, 102, 153);
        }
        .green {
          color: rgb(0, 136, 24);
        }
        .pink {
          color: rgb(126, 0, 146);
        }
        .hui{
            color: #7b6542;
        }
      }
    }
  }
}
.inline {
    
  overflow: hidden;
  width: 3.55rem;
  margin: 0 auto 0.15rem;
  border-radius: 0.05rem;
  box-shadow: 0 0 8px #ccc;
  background: #fff;
  .read-top {
    width: 100%;
    height: 0.55rem;
    img {
      width: 100%;
      height: 100%;
    }
  }
  .aviation_text {
    border-radius: 0.04rem;
    // margin: 0 0.1rem;
    margin-top: 0.15rem;
    margin-bottom: 0.15rem;
    overflow: hidden;
    background-color: #fff;
    ::v-deep .ant-form-item-control {
      display: flex;
      flex-direction: column;
      width: 3.55rem;
      // width: 2.73rem;
      // margin: 0 auto;
    }
    .aviation_text_content {
      display: flex;
      flex-direction: column;
      padding-top: 0.15rem;
      .aviation_text_input {
        display: flex;
        // justify-content: center;
        align-items: center;
        margin-bottom: 0.1rem;
        .span {
          width: 0.8rem;
          line-height: 0.35rem;
          color: #454444;
          margin-left: 0.3rem;
          em {
            color: #e76888;
          }
        }
        .ant-calendar-picker {
          width: 2rem;
        }
        input {
          // width: 2.52rem;
          width: 2rem;
          border-radius: 0;
          height: 0.35rem;
          color: #000;
        }
      }
      .aviation_textarea {
        display: flex;
        span {
          width: 0.75rem;
          height: 0.35rem;
          font-family: PingFang-SC-Medium;
          font-weight: normal;
          font-stretch: normal;
          letter-spacing: 0px;
          // color: #333333;
          padding-left: 0.05rem;
          line-height: 0.35rem;
          color: #454444;
          margin-left: 0.3rem;
        }
        .aviation_textarea_text {
          border: 1px solid #cbcbcb;
          width: 2rem;
          textarea {
            width: 1.75rem;
            height: 0.63rem;
            border-radius: 0.01rem;
            padding-left: 0.14rem;
            padding-top: 0.11rem;
            border: none;
            outline: none;
            resize: none;
          }
          textarea::-webkit-input-placeholder {
            /* WebKit browsers*/
            color: #cbcbcb;
          }
        }
      }
      .aviation_text_cascader {
        display: flex;
        // justify-content: center;
        //   align-items: center;
        margin-bottom: 0.1rem;
        .span {
          width: 0.8rem;
          // text-align: center;
          line-height: 0.35rem;
          color: #454444;
          margin-left: 0.3rem;
          em {
            color: #e76888;
          }
        }
        .ant-cascader-picker {
          width: 2rem;
        }
        .from_three {
          position: relative;
          height: 0.35rem;
          .ant-select-selection-selected-value {
            display: inline-block !important;
            padding-left: 0.05rem;
            color: #000 !important;
          }
        }
      }
      .bottom_jick {
        margin: 0.15rem 0 auto;
        .aviation_text_button {
          background: #1d6da5;
          width: 2.73rem;
          height: 0.44rem;
          display: block;
          // margin: 0.1rem 0.5rem 0 0.5rem;
          margin: 0 auto;
          line-height: 0.44rem;
          text-align: center;
          font-size: 0.18rem;
          color: #e8ffff;
        }
        .submit-size {
          height: 0.13rem;
          text-align: center;
          padding-bottom: 0.15rem;
          display: block;
          // padding: 0 0 0.03rem 0;
          padding-top: 0.05rem;
          font-family: PingFang-SC-Medium;
          font-weight: normal;
          font-stretch: normal;
          line-height: 18px;
          letter-spacing: 0px;
          color: #888888;
        }
      }
    }
  }
  ::v-deep .ant-select-selection {
    border-radius: 0 !important;
    z-index: 99;
    font-size: 14px;
    padding-left: 0.05rem;
  }
  ::v-deep .ant-select-selection--single {
    height: 0.35rem;
    i {
      svg {
        width: 10px;
        height: 9px;
        font-family: PingFang-SC-Medium;
        font-size: 12px;
        font-weight: normal;
        font-stretch: normal;
        line-height: 18px;
        letter-spacing: 0px;
        color: #888888;
      }
    }
  }
  ::v-deep .ant-select-selection__rendered {
    line-height: 0.35rem;
  }
  ::v-deep .ant-calendar-picker-input {
    height: 0.35rem;
  }
  ::v-deep .ant-input {
    height: 0.35rem;
    display: inline-block;
    padding-left: 0.15rem;
    color: #000;
    margin-right: 0.38rem;
    border-radius: 0;
  }
  .ant-form-item {
    margin: 0;
  }
  ::v-deep .ant-col-offset-4 {
    margin: 0 !important;
  }
  ::v-deep .ant-form-explain {
    text-align: center;
    padding-left: 0.25rem;
    padding-bottom: 0.05rem;
  }
}
.cdsa {
  overflow: hidden;
  width: 3.55rem;
  margin: 0 auto 0.15rem;
  border-radius: 0.05rem;
  box-shadow: 0 0 8px #ccc;
  background: #fff;
}
.read {
  width: 3.55rem;
  margin: 0 auto 0.15rem;
  background: #fff;
  padding-bottom: 0.3rem;
  border-radius: 5px;
  overflow: hidden;
  .read-top {
    width: 100%;
    height: 0.55rem;
    img {
      width: 100%;
      height: 100%;
    }
  }
  .data {
    width: 100%;
    .data-cont {
      padding-left: 0.15rem;
      margin-top: 0.2rem;
      height: 0.35rem;
      .left {
        width: 0.47rem;
        height: 0.35rem;
        border-right: 1px solid rgb(204, 204, 204);
        font-size: 0.09rem;
        float: left;
        color: rgb(153, 153, 153);
        text-align: center;
        p:first-of-type {
          font-size: 0.2rem;
          height: 0.2rem;
          line-height: 0.2rem;
        }
      }
      .right {
        float: left;
        margin-left: 0.08rem;
        line-height: 0.13rem;
        color: rgb(102, 102, 102);
        font-size: 0.13rem;
        p:first-of-type {
          font-size: 0.15rem;
          line-height: 0.15rem;
          color: rgb(51, 51, 51);
          margin-bottom: 0.07rem;
        }
      }
    }
  }
}
</style>
