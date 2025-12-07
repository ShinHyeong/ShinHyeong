# ShinHyeong Park
## About Me
- 🎓 BS, Kangwon National University, Computer Science major (2018.03 - 2025.08)
- 👀 interested in **Backend Web Development**
- 📫 How to reach me : shinhyeong.dev@gmail.com
- 📝 I record and share my study notes for backend technologies, including Java, Spring Boot, and CS and problem-solving processes in my projects. [Visit my tech blog ↗](https://shinhyeong.github.io/)

## Latest Blog Posts
<table>
  <tr>
    <th width="20%">Date</th>
    <th width="80%">Recent Posts</th>
  </tr>
  <!-- BLOG-POST-LIST:START --><tr><td width='20%'>DATE</td><td width='80%'><a href='https://shinhyeong.github.io/aws-saa/aws-saa-classic-architecture/'><b>Chapter1. Classic Architecture</b></a><br/>&lt;h1 id=&quot;1-서버&quot;&gt;1. 서버&lt;/h1&gt;

&lt;h2 id=&quot;1-elastic-compute-cloudec2&quot;&gt;1&rpar; Elastic Compute Cloud&lpar;EC2&rpar;&lt;/h2&gt;

&lt;h3 id=&quot;무엇이든-뭔가-하려면-일단-컴퓨터가-필요하다&quot;&gt;무엇이든 뭔가 하려면 일단 컴퓨터가 필요하다.&lt;/h3&gt;

&lt;p class=&quot;story-box&quot;&gt;우리가 컴퓨터를 사용하는 목적은 다양하지만, 개발자에게 있어 컴퓨터는 곧 &lt;strong class=&quot;highlight-text&quot;&gt;서비스를 제공하기 위한 도구&lt;/strong&gt;입니다. 단순히 게임을 하거나 동영상을 시청하는 것이 아니라&lpar;소비&rpar;, 무언가를 사용자에게 전달하는 역할을 수행하는 것이죠.&lt;/p&gt;

&lt;div class=&quot;info-box&quot;&gt;
  &lt;div style=&quot;max-width: 800px; margin: 0 auto; background-color: #f8fafc; padding: 1.5rem; border-radius: 1rem; border: 1px solid #e2e8f0; font-family: sans-serif; color: #333; box-sizing: border-box;&quot;&gt;
    
    &lt;h4 style=&quot;text-align: center; margin-top: 0; font-size: 1.2rem; font-weight: 800; color: #1e293b; margin-bottom: 1.5rem;&quot;&gt;
      &lt;i class=&quot;fas fa-cloud&quot; style=&quot;color: #f97316; margin-right: 0.5rem;&quot;&gt;&lt;/i&gt;
      EC2 = 우리가 빌린 &#39;웨이터&lpar;Server&rpar;&#39;
    &lt;/h4&gt;

    &lt;div style=&quot;display: flex; flex-wrap: wrap; justify-content: center; align-items: center; gap: 0.8rem;&quot;&gt;

      &lt;div style=&quot;flex: 1; min-width: 200px; display: flex; flex-direction: column; gap: 0.8rem;&quot;&gt;
        &lt;div style=&quot;background: white; padding: 0.8rem; border-radius: 0.75rem; border: 1px solid #e2e8f0; box-shadow: 0 2px 4px rgba&lpar;0,0,0,0.05&rpar;; position: relative;&quot;&gt;
          &lt;span style=&quot;position: absolute; top: -0.5rem; left: 0.8rem; background: #64748b; color: white; padding: 0.1rem 0.5rem; border-radius: 4px; font-size: 0.65rem; font-weight: 700;&quot;&gt;비유&lt;/span&gt;
          &lt;div style=&quot;display: flex; align-items: center; justify-content: space-between; margin-top: 0.3rem;&quot;&gt;
            &lt;div style=&quot;text-align: center;&quot;&gt;
              &lt;span style=&quot;font-size: 1.8rem;&quot;&gt;🙋‍♂️&lt;/span&gt;&lt;br /&gt;
              &lt;span style=&quot;font-size: 0.7rem; font-weight: 700; color: #64748b;&quot;&gt;손님&lt;/span&gt;
            &lt;/div&gt;
            &lt;div style=&quot;color: #cbd5e1; font-size: 1rem;&quot;&gt;
              &lt;i class=&quot;fas fa-arrow-right&quot;&gt;&lt;/i&gt;
            &lt;/div&gt;
            &lt;div style=&quot;text-align: center;&quot;&gt;
              &lt;span style=&quot;font-size: 1.8rem;&quot;&gt;🗣️&lt;/span&gt;&lt;br /&gt;
              &lt;span style=&quot;font-size: 0.7rem; font-weight: 700; color: #1e293b;&quot;&gt;주문&lt;/span&gt;
            &lt;/div&gt;
          &lt;/div&gt;
        &lt;/div&gt;

        &lt;div style=&quot;background: white; padding: 0.8rem; border-radius: 0.75rem; border: 1px solid #e2e8f0; box-shadow: 0 2px 4px rgba&lpar;0,0,0,0.05&rpar;; position: relative;&quot;&gt;
          &lt;span style=&quot;position: absolute; top: -0.5rem; left: 0.8rem; background: #3b82f6; color: white; padding: 0.1rem 0.5rem; border-radius: 4px; font-size: 0.65rem; font-weight: 700;&quot;&gt;실제&lt;/span&gt;
          &lt;div style=&quot;display: flex; align-items: center; justify-content: space-between; margin-top: 0.3rem;&quot;&gt;
            &lt;div style=&quot;text-align: center;&quot;&gt;
              &lt;span style=&quot;font-size: 1.8rem;&quot;&gt;💻&lt;/span&gt;&lt;br /&gt;
              &lt;span style=&quot;font-size: 0.7rem; font-weight: 700; color: #64748b;&quot;&gt;사용자&lt;/span&gt;
            &lt;/div&gt;
            &lt;div style=&quot;color: #cbd5e1; font-size: 1rem;&quot;&gt;
              &lt;i class=&quot;fas fa-arrow-right&quot;&gt;&lt;/i&gt;
            &lt;/div&gt;
            &lt;div style=&quot;text-align: center;&quot;&gt;
              &lt;span style=&quot;font-size: 1.8rem;&quot;&gt;🖱️&lt;/span&gt;&lt;br /&gt;
              &lt;span style=&quot;font-size: 0.7rem; font-weight: 700; color: #1e293b;&quot;&gt;클릭&lpar;요청&rpar;&lt;/span&gt;
            &lt;/div&gt;
          &lt;/div&gt;
        &lt;/div&gt;
      &lt;/div&gt;

      &lt;div style=&quot;flex: 0 0 auto; z-index: 10;&quot;&gt;
        &lt;div style=&quot;background: linear-gradient&lpar;135deg, #fff7ed 0%, #ffedd5 100%&rpar;; padding: 1rem; border-radius: 1rem; border: 2px solid #f97316; box-shadow: 0 10px 25px -5px rgba&lpar;249, 115, 22, 0.4&rpar;; text-align: center; width: 170px; display: flex; flex-direction: column; justify-content: center; align-items: center; position: relative; box-sizing: border-box;&quot;&gt;

          &lt;div style=&quot;position: relative; display: inline-block; margin-bottom: 0.3rem;&quot;&gt;
            &lt;i class=&quot;fas fa-server&quot; style=&quot;font-size: 3.5rem; color: #fdba74;&quot;&gt;&lt;/i&gt;
            &lt;div style=&quot;position: absolute; bottom: -5px; right: -8px; background: white; border-radius: 50%; padding: 4px; box-shadow: 0 2px 4px rgba&lpar;0,0,0,0.1&rpar;;&quot;&gt;
                &lt;span style=&quot;font-size: 2rem; line-height: 1;&quot;&gt;🤵&lt;/span&gt;
            &lt;/div&gt;
          &lt;/div&gt;

          &lt;h4 style=&quot;margin: 0.3rem 0 0; font-size: 1.1rem; font-weight: 800; color: #c2410c;&quot;&gt;AWS EC2&lt;/h4&gt;
          &lt;span style=&quot;font-size: 0.75rem; font-weight: 600; color: #ea580c; background: rgba&lpar;255,255,255,0.6&rpar;; padding: 0.2rem 0.5rem; border-radius: 99px; margin-top: 0.3rem; display: inline-block;&quot;&gt;
            = 서버 &lpar;가상 PC&rpar;
          &lt;/span&gt;

          &lt;i class=&quot;fas fa-chevron-right&quot; style=&quot;position: absolute; left: -14px; top: 50%; transform: translateY&lpar;-50%&rpar;; font-size: 1.2rem; color: #f97316;&quot;&gt;&lt;/i&gt;
          &lt;i class=&quot;fas fa-chevron-right&quot; style=&quot;position: absolute; right: -14px; top: 50%; transform: translateY&lpar;-50%&rpar;; font-size: 1.2rem; color: #3b82f6;&quot;&gt;&lt;/i&gt;
        &lt;/div&gt;
      &lt;/div&gt;

      &lt;div style=&quot;flex: 1; min-width: 200px; display: flex; flex-direction: column; gap: 0.8rem;&quot;&gt;
        &lt;div style=&quot;background: white; padding: 0.8rem; border-radius: 0.75rem; border: 1px solid #e2e8f0; box-shadow: 0 2px 4px rgba&lpar;0,0,0,0.05&rpar;; position: relative;&quot;&gt;
          &lt;span style=&quot;position: absolute; top: -0.5rem; right: 0.8rem; background: #64748b; color: white; padding: 0.1rem 0.5rem; border-radius: 4px; font-size: 0.65rem; font-weight: 700;&quot;&gt;비유&lt;/span&gt;
          &lt;div style=&quot;display: flex; align-items: center; justify-content: space-between; margin-top: 0.3rem;&quot;&gt;
            &lt;div style=&quot;text-align: center;&quot;&gt;
              &lt;span style=&quot;font-size: 1.8rem;&quot;&gt;🍲&lt;/span&gt;&lt;br /&gt;
              &lt;span style=&quot;font-size: 0.7rem; font-weight: 700; color: #1e293b;&quot;&gt;음식&lt;/span&gt;
            &lt;/div&gt;
            &lt;div style=&quot;color: #cbd5e1; font-size: 1rem;&quot;&gt;
              &lt;i class=&quot;fas fa-arrow-right&quot;&gt;&lt;/i&gt;
            &lt;/div&gt;
            &lt;div style=&quot;text-align: center;&quot;&gt;
              &lt;span style=&quot;font-size: 1.8rem;&quot;&gt;😋&lt;/span&gt;&lt;br /&gt;
              &lt;span style=&quot;font-size: 0.7rem; font-weight: 700; color: #64748b;&quot;&gt;서빙 완료&lt;/span&gt;
            &lt;/div&gt;
          &lt;/div&gt;
        &lt;/div&gt;

        &lt;div style=&quot;background: white; padding: 0.8rem; border-radius: 0.75rem; border: 1px solid #e2e8f0; box-shadow: 0 2px 4px rgba&lpar;0,0,0,0.05&rpar;; position: relative;&quot;&gt;
          &lt;span style=&quot;position: absolute; top: -0.5rem; right: 0.8rem; background: #3b82f6; color: white; padding: 0.1rem 0.5rem; border-radius: 4px; font-size: 0.65rem; font-weight: 700;&quot;&gt;실제&lt;/span&gt;
          &lt;div style=&quot;display: flex; align-items: center; justify-content: space-between; margin-top: 0.3rem;&quot;&gt;
            &lt;div style=&quot;text-align: center;&quot;&gt;
              &lt;span style=&quot;font-size: 1.8rem;&quot;&gt;🎬&lt;/span&gt;&lt;br /&gt;
              &lt;span style=&quot;font-size: 0.7rem; font-weight: 700; color: #1e293b;&quot;&gt;영상 파일&lt;/span&gt;
            &lt;/div&gt;
            &lt;div style=&quot;color: #cbd5e1; font-size: 1rem;&quot;&gt;
              &lt;i class=&quot;fas fa-arrow-right&quot;&gt;&lt;/i&gt;
            &lt;/div&gt;
            &lt;div style=&quot;text-align: center;&quot;&gt;
              &lt;span style=&quot;font-size: 1.8rem;&quot;&gt;📺&lt;/span&gt;&lt;br /&gt;
              &lt;span style=&quot;font-size: 0.7rem; font-weight: 700; color: #64748b;&quot;&gt;화면 재생&lt;/span&gt;
            &lt;/div&gt;
          &lt;/div&gt;
        &lt;/div&gt;
      &lt;/div&gt;

    &lt;/div&gt;

    &lt;div style=&quot;text-align: center; margin-top: 1.5rem; background-color: #fff; padding: 1rem; border-radius: 0.5rem; border: 1px solid #e2e8f0;&quot;&gt;
      &lt;p style=&quot;margin: 0; font-size: 0.9rem; line-height: 1.6; color: #475569;&quot;&gt;
        우리가 AWS에서 빌리는 &lt;strong&gt;EC2 인스턴스&lt;/strong&gt;가 바로&lt;br /&gt;
        주문&lpar;요청&rpar;을 처리하고 음식&lpar;결과&rpar;을 가져다주는 &lt;strong&gt;웨이터&lpar;Server&rpar;&lt;/strong&gt; 역할을 합니다.
      &lt;/p&gt;
    &lt;/div&gt;

  &lt;/div&gt;
&lt;/div&gt;

&lt;div class=&quot;story-box&quot;&gt;
  &lt;p&gt;&lt;strong&gt;‘서버&lpar;Server&rpar;’&lt;/strong&gt;라는 의미를 식당으로 비유를 들어보겠습니다.&lt;/p&gt;

  &lt;ol&gt;
    &lt;li&gt;&lt;strong&gt;주문 &lpar;요청&rpar;&lt;/strong&gt;: 식당에 방문한 손님&lpar;사용자&rpar;이 웨이터&lpar;Server&rpar;에게 음식을 주문합니다.
      &lt;ul&gt;
        &lt;li&gt;예시: 넷플릭스 앱에서 &lt;strong&gt;‘오징어 게임 시즌2 1화’&lt;/strong&gt;를 &lt;strong&gt;클릭&lpar;요청&rpar;&lt;/strong&gt;합니다.&lt;/li&gt;
      &lt;/ul&gt;
    &lt;/li&gt;
    &lt;li&gt;&lt;strong&gt;서빙 &lpar;제공&rpar;&lt;/strong&gt;: 웨이터는 주문받은 음식을 주방에서 가져와 손님에게 &lt;strong&gt;서빙&lpar;제공&rpar;&lt;/strong&gt;합니다.
      &lt;ul&gt;
        &lt;li&gt;예시: 요청을 받은 서버는 저장된 영상 파일을 사용자에게 &lt;strong&gt;스트리밍&lpar;제공&rpar;&lt;/strong&gt;합니다.&lt;/li&gt;
      &lt;/ul&gt;
    &lt;/li&gt;
  &lt;/ol&gt;

  &lt;p&gt;AWS의 &lt;strong&gt;Elastic Compute Cloud &lpar;EC2&rpar;&lt;/strong&gt;는 바로 이 ‘서버’ 역할을 하는 가상 컴퓨터를 클라우드 환경에서 빌려 쓰는 서비스입니다. 즉, 넷플릭스 사용자의 요청에 따라 영상을 찾아 서빙해 주는 &lt;strong&gt;‘웨이터’&lt;/strong&gt;를 AWS에서 고용하는 것과 같습니다.&lt;/p&gt;

  &lt;p&gt;EC2는 본질적으로 컴퓨터이기 때문에 다음과 같은 특징을 가집니다.&lt;/p&gt;

  &lt;ul&gt;
    &lt;li&gt;🖥️ &lt;strong class=&quot;highlight-text&quot;&gt;컴퓨터로서의 기본 기능&lt;/strong&gt; : 일반 PC처럼 CPU, RAM, 스토리지, 네트워크, IP 등을 가짐&lt;/li&gt;
    &lt;li&gt;🛡️ &lt;strong class=&quot;highlight-text&quot;&gt;‘서버’로서의 특화 기능&lt;/strong&gt; : 서비스 제공을 위해 보안&lpar;Security&rpar;, 비용 관리, 개발 편의 사항 등이 각별하게 신경 써져 있음&lt;/li&gt;
  &lt;/ul&gt;
&lt;/div&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;h3 id=&quot;주요-연관-기능&quot;&gt;주요 연관 기능&lt;/h3&gt;

&lt;p class=&quot;story-box&quot;&gt;EC2는 혼자서 독립적으로 존재하기보다, AWS의 생태계 안에서 다른 핵심 서비스들과 유기적으로 연결될 때 비로소 &lt;strong class=&quot;highlight-text&quot;&gt;안정적인 서비스 운영&lt;/strong&gt;이 가능해집니다.&lt;/p&gt;

&lt;div class=&quot;info-box&quot;&gt;
    
    &lt;div style=&quot;padding: 0 1.5rem; display: flex; gap: 1rem; flex-wrap: wrap; justify-content: center;&quot;&gt;

      &lt;div style=&quot;flex: 1; min-width: 140px; background-color: #ffffff; padding: 1rem; border-radius: 0.5rem; border: 1px solid #e2e8f0; box-shadow: 0 1px 2px 0 rgba&lpar;0, 0, 0, 0.05&rpar;; text-align: center; display: flex; flex-direction: column; align-items: center;&quot;&gt;
        &lt;i class=&quot;fas fa-server&quot; style=&quot;font-size: 2rem; color: #94a3b8; margin-bottom: 0.5rem;&quot;&gt;&lt;/i&gt;
        &lt;h4 style=&quot;margin: 0.2rem 0; font-size: 1rem; font-weight: 700; color: #1e293b;&quot;&gt;EC2&lt;/h4&gt;
        &lt;span style=&quot;font-size: 0.85rem; color: #64748b;&quot;&gt;가상 머신&lt;/span&gt;
      &lt;/div&gt;

      &lt;div style=&quot;flex: 1; min-width: 140px; background-color: #ffffff; padding: 1rem; border-radius: 0.5rem; border: 1px solid #e2e8f0; box-shadow: 0 1px 2px 0 rgba&lpar;0, 0, 0, 0.05&rpar;; text-align: center; display: flex; flex-direction: column; align-items: center;&quot;&gt;
        &lt;i class=&quot;far fa-hdd&quot; style=&quot;font-size: 2rem; color: #94a3b8; margin-bottom: 0.5rem;&quot;&gt;&lt;/i&gt;
        &lt;h4 style=&quot;margin: 0.2rem 0; font-size: 1rem; font-weight: 700; color: #1e293b;&quot;&gt;EBS&lt;/h4&gt;
        &lt;span style=&quot;font-size: 0.85rem; color: #64748b;&quot;&gt;데이터 저장&lt;/span&gt;
      &lt;/div&gt;

      &lt;div style=&quot;flex: 1; min-width: 140px; background-color: #ffffff; padding: 1rem; border-radius: 0.5rem; border: 1px solid #e2e8f0; box-shadow: 0 1px 2px 0 rgba&lpar;0, 0, 0, 0.05&rpar;; text-align: center; display: flex; flex-direction: column; align-items: center;&quot;&gt;
        &lt;i class=&quot;fas fa-network-wired&quot; style=&quot;font-size: 2rem; color: #94a3b8; margin-bottom: 0.5rem;&quot;&gt;&lt;/i&gt;
        &lt;h4 style=&quot;margin: 0.2rem 0; font-size: 1rem; font-weight: 700; color: #1e293b;&quot;&gt;ELB&lt;/h4&gt;
        &lt;span style=&quot;font-size: 0.85rem; color: #64748b;&quot;&gt;부하 분산&lt;/span&gt;
      &lt;/div&gt;

      &lt;div style=&quot;flex: 1; min-width: 140px; background-color: #ffffff; padding: 1rem; border-radius: 0.5rem; border: 1px solid #e2e8f0; box-shadow: 0 1px 2px 0 rgba&lpar;0, 0, 0, 0.05&rpar;; text-align: center; display: flex; flex-direction: column; align-items: center;&quot;&gt;
        &lt;i class=&quot;fas fa-layer-group&quot; style=&quot;font-size: 2rem; color: #94a3b8; margin-bottom: 0.5rem;&quot;&gt;&lt;/i&gt;
        &lt;h4 style=&quot;margin: 0.2rem 0; font-size: 1rem; font-weight: 700; color: #1e293b;&quot;&gt;ASG&lt;/h4&gt;
        &lt;span style=&quot;font-size: 0.85rem; color: #64748b;&quot;&gt;자동 확장&lt;/span&gt;
      &lt;/div&gt;

    &lt;/div&gt;
&lt;/div&gt;

&lt;div class=&quot;story-box&quot;&gt;
  &lt;p&gt;가장 대표적으로 함께 사용되는 기능들은 다음과 같습니다.&lt;/p&gt;

  &lt;ol&gt;
    &lt;li&gt;&lt;strong&gt;EBS &lpar;Elastic Block Store&rpar;&lt;/strong&gt;
      &lt;ul&gt;
        &lt;li&gt;EC2가 연산&lpar;CPU, RAM&rpar;을 담당하는 두뇌라면, EBS는 데이터를 영구적으로 보관하는 &lt;strong class=&quot;highlight-text&quot;&gt;저장소&lpar;SSD/HDD&rpar;&lt;/strong&gt;입니다.&lt;/li&gt;
        &lt;li&gt;EC2 인스턴스를 중지하거나 종료해도 중요한 데이터가 사라지지 않도록 별도로 저장하는 ‘외장 하드’와 같은 역할을 합니다.&lt;/li&gt;
      &lt;/ul&gt;
    &lt;/li&gt;
    &lt;li&gt;&lt;strong&gt;ELB &lpar;Elastic Load Balancing&rpar;&lt;/strong&gt;
      &lt;ul&gt;
        &lt;li&gt;맛집에 손님이 몰리면 웨이터 한 명으로는 감당이 안 되듯, 접속자가 폭주하면 서버 한 대로는 부족할 수 있습니다.&lt;/li&gt;
        &lt;li&gt;ELB는 들어오는 트래픽&lpar;손님&rpar;을 여러 대의 EC2 인스턴스에 골고루 나눠주는 &lt;strong class=&quot;highlight-text&quot;&gt;부하 분산 장치&lpar;매니저&rpar;&lt;/strong&gt; 역할을 수행합니다.&lt;/li&gt;
      &lt;/ul&gt;
    &lt;/li&gt;
    &lt;li&gt;&lt;strong&gt;ASG &lpar;Auto Scaling Group&rpar;&lt;/strong&gt;
      &lt;ul&gt;
        &lt;li&gt;서비스 사용량은 항상 일정하지 않습니다. 낮에는 많고 새벽에는 적을 수 있습니다.&lt;/li&gt;
        &lt;li&gt;ASG는 트래픽 양에 맞춰 EC2 인스턴스의 개수를 자동으로 늘리거나&lpar;Scale-out&rpar; 줄여주는&lpar;Scale-in&rpar; &lt;strong class=&quot;highlight-text&quot;&gt;자동 확장 기능&lt;/strong&gt;입니다. 이를 통해 비용 효율성을 극대화할 수 있습니다.&lt;/li&gt;
      &lt;/ul&gt;
    &lt;/li&gt;
  &lt;/ol&gt;
&lt;/div&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;h3 id=&quot;인스턴스-유형&quot;&gt;인스턴스 유형&lt;/h3&gt;

&lt;div class=&quot;story-box&quot;&gt;
  &lt;p&gt;EC2 인스턴스를 생성하려고 보면 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;t3.small&lt;/code&gt;, &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;m5.large&lt;/code&gt; 같은 암호 같은 이름들을 마주하게 됩니다. 하지만 이 이름에는 규칙이 있습니다. 바로 &lt;strong&gt;[패밀리] + [세대] + [크기]&lt;/strong&gt; 순서입니다.&lt;/p&gt;

  &lt;ul&gt;
    &lt;li&gt;&lt;strong&gt;패밀리&lpar;Family&rpar;:&lt;/strong&gt; 인스턴스의 특성 &lpar;앞글자 알파벳&rpar;&lt;/li&gt;
    &lt;li&gt;&lt;strong&gt;세대&lpar;Generation&rpar;:&lt;/strong&gt; 숫자가 높을수록 최신 모델&lt;/li&gt;
    &lt;li&gt;&lt;strong&gt;크기&lpar;Size&rpar;:&lt;/strong&gt; CPU와 메모리의 용량 &lpar;nano &amp;lt; micro &amp;lt; small &amp;lt; medium &amp;lt; large …&rpar;&lt;/li&gt;
  &lt;/ul&gt;

  &lt;p&gt;가장 중요한 것은 &lt;strong&gt;‘맨 앞글자&lpar;패밀리&rpar;’&lt;/strong&gt;가 무엇이냐에 따라 사용 목적이 완전히 달라진다는 점입니다.&lt;/p&gt;
&lt;/div&gt;

&lt;div class=&quot;info-box&quot;&gt;
  &lt;div style=&quot;padding: 0 1.5rem; border-radius: 1rem; max-width: 800px; margin: 0 auto;&quot;&gt;

    &lt;div style=&quot;background-color: #f8fafc; border-radius: 0.5rem; padding: 0.8rem; margin-bottom: 1.5rem; display: flex; justify-content: center; align-items: center; gap: 0.5rem; font-size: 0.85rem;&quot;&gt;
      &lt;div style=&quot;text-align: center;&quot;&gt;
        &lt;span style=&quot;background: #eff6ff; color: #2563eb; border: 1px solid #bfdbfe; padding: 0.1rem 0.4rem; border-radius: 3px; font-weight: 700;&quot;&gt;t&lt;/span&gt;
        &lt;span style=&quot;font-size: 0.75rem; color: #64748b; margin-left: 0.2rem;&quot;&gt;클래스&lpar;패밀리&rpar;&lt;/span&gt;
      &lt;/div&gt;
      &lt;span style=&quot;color: #cbd5e1; font-weight: 700;&quot;&gt;•&lt;/span&gt;
      &lt;div style=&quot;text-align: center;&quot;&gt;
        &lt;span style=&quot;background: #f0fdf4; color: #16a34a; border: 1px solid #bbf7d0; padding: 0.1rem 0.4rem; border-radius: 3px; font-weight: 700;&quot;&gt;3&lt;/span&gt;
        &lt;span style=&quot;font-size: 0.75rem; color: #64748b; margin-left: 0.2rem;&quot;&gt;세대&lt;/span&gt;
      &lt;/div&gt;
      &lt;span style=&quot;color: #cbd5e1; font-weight: 700;&quot;&gt;•&lt;/span&gt;
      &lt;div style=&quot;text-align: center;&quot;&gt;
        &lt;span style=&quot;background: #faf5ff; color: #9333ea; border: 1px solid #e9d5ff; padding: 0.1rem 0.4rem; border-radius: 3px; font-weight: 700;&quot;&gt;small&lt;/span&gt;
        &lt;span style=&quot;font-size: 0.75rem; color: #64748b; margin-left: 0.2rem;&quot;&gt;크기&lt;/span&gt;
      &lt;/div&gt;
    &lt;/div&gt;

    &lt;div style=&quot;display: flex; flex-direction: column; gap: 0.6rem;&quot;&gt;

      &lt;div style=&quot;background-color: #fff; border: 1px solid #e2e8f0; border-radius: 0.5rem; padding: 0.8rem; display: flex; align-items: flex-start; gap: 0.8rem;&quot;&gt;
        &lt;div style=&quot;background-color: #eff6ff; width: 36px; height: 36px; display: flex; align-items: center; justify-content: center; border-radius: 0.3rem; color: #2563eb; font-weight: 800; font-size: 1.1rem; flex-shrink: 0;&quot;&gt;m&lt;/div&gt;
        &lt;div style=&quot;flex: 1; min-width: 0;&quot;&gt;
          &lt;div style=&quot;display: flex; align-items: center; gap: 0.4rem; margin-bottom: 0.3rem; white-space: nowrap; overflow: hidden;&quot;&gt;
            &lt;span style=&quot;font-weight: 800; font-size: 0.9rem; color: #1e293b;&quot;&gt;범용&lt;/span&gt;
            &lt;span style=&quot;font-size: 0.75rem; color: #64748b;&quot;&gt;&lpar;General Purpose&rpar;&lt;/span&gt;
            &lt;span style=&quot;font-size: 0.65rem; color: #1e40af; background: #dbeafe; padding: 0.1rem 0.3rem; border-radius: 3px; font-weight: 700;&quot;&gt;Hint: Modest&lt;/span&gt;
          &lt;/div&gt;
          &lt;div style=&quot;font-size: 0.8rem; line-height: 1.6; color: #475569;&quot;&gt;
            컴퓨팅/메모리/네트워크 &lt;strong&gt;균형&lt;/strong&gt;
            &lt;span style=&quot;background:#f1f5f9; padding:0 0.3rem; border-radius:3px; color:#475569; margin-left:0.2rem;&quot;&gt;웹 서버&lt;/span&gt;
            &lt;span style=&quot;background:#f1f5f9; padding:0 0.3rem; border-radius:3px; color:#475569;&quot;&gt;코드 저장소&lt;/span&gt;
          &lt;/div&gt;
        &lt;/div&gt;
      &lt;/div&gt;

      &lt;div style=&quot;background-color: #fff; border: 1px solid #e2e8f0; border-radius: 0.5rem; padding: 0.8rem; display: flex; align-items: flex-start; gap: 0.8rem;&quot;&gt;
        &lt;div style=&quot;background-color: #fff7ed; width: 36px; height: 36px; display: flex; align-items: center; justify-content: center; border-radius: 0.3rem; color: #ea580c; font-weight: 800; font-size: 1.1rem; flex-shrink: 0;&quot;&gt;c&lt;/div&gt;
        &lt;div style=&quot;flex: 1; min-width: 0;&quot;&gt;
          &lt;div style=&quot;display: flex; align-items: center; gap: 0.4rem; margin-bottom: 0.3rem; white-space: nowrap; overflow: hidden;&quot;&gt;
            &lt;span style=&quot;font-weight: 800; font-size: 0.9rem; color: #1e293b;&quot;&gt;컴퓨팅 최적화&lt;/span&gt;
            &lt;span style=&quot;font-size: 0.75rem; color: #64748b;&quot;&gt;&lpar;Compute&rpar;&lt;/span&gt;
            &lt;span style=&quot;font-size: 0.65rem; color: #9a3412; background: #ffedd5; padding: 0.1rem 0.3rem; border-radius: 3px; font-weight: 700;&quot;&gt;Hint: Computing&lt;/span&gt;
          &lt;/div&gt;
          &lt;div style=&quot;font-size: 0.8rem; line-height: 1.6; color: #475569;&quot;&gt;
            &lt;strong&gt;고성능 프로세서&lt;/strong&gt; 필요 작업
            &lt;span style=&quot;background:#f1f5f9; padding:0 0.3rem; border-radius:3px; color:#475569; margin-left:0.2rem;&quot;&gt;배치 처리&lt;/span&gt;
            &lt;span style=&quot;background:#f1f5f9; padding:0 0.3rem; border-radius:3px; color:#475569;&quot;&gt;고성능 웹서버&lt;/span&gt;
            &lt;span style=&quot;background:#f1f5f9; padding:0 0.3rem; border-radius:3px; color:#475569;&quot;&gt;미디어/AI&lt;/span&gt;
          &lt;/div&gt;
        &lt;/div&gt;
      &lt;/div&gt;

      &lt;div style=&quot;background-color: #fff; border: 1px solid #e2e8f0; border-radius: 0.5rem; padding: 0.8rem; display: flex; align-items: flex-start; gap: 0.8rem;&quot;&gt;
        &lt;div style=&quot;background-color: #f0fdf4; width: 36px; height: 36px; display: flex; align-items: center; justify-content: center; border-radius: 0.3rem; color: #16a34a; font-weight: 800; font-size: 1.1rem; flex-shrink: 0;&quot;&gt;r&lt;/div&gt;
        &lt;div style=&quot;flex: 1; min-width: 0;&quot;&gt;
          &lt;div style=&quot;display: flex; align-items: center; gap: 0.4rem; margin-bottom: 0.3rem; white-space: nowrap; overflow: hidden;&quot;&gt;
            &lt;span style=&quot;font-weight: 800; font-size: 0.9rem; color: #1e293b;&quot;&gt;메모리 최적화&lt;/span&gt;
            &lt;span style=&quot;font-size: 0.75rem; color: #64748b;&quot;&gt;&lpar;Memory&rpar;&lt;/span&gt;
            &lt;span style=&quot;font-size: 0.65rem; color: #166534; background: #dcfce7; padding: 0.1rem 0.3rem; border-radius: 3px; font-weight: 700;&quot;&gt;Hint: RAM&lt;/span&gt;
          &lt;/div&gt;
          &lt;div style=&quot;font-size: 0.8rem; line-height: 1.6; color: #475569;&quot;&gt;
            &lt;strong&gt;빠른 성능&lt;/strong&gt; 및 메모리 내 대규모 데이터 처리
            &lt;span style=&quot;background:#f1f5f9; padding:0 0.3rem; border-radius:3px; color:#475569; margin-left:0.2rem;&quot;&gt;실시간 빅데이터&lt;/span&gt;
            &lt;span style=&quot;background:#f1f5f9; padding:0 0.3rem; border-radius:3px; color:#475569;&quot;&gt;고성능 DB&lt;/span&gt;
          &lt;/div&gt;
        &lt;/div&gt;
      &lt;/div&gt;

      &lt;div style=&quot;background-color: #fff; border: 1px solid #e2e8f0; border-radius: 0.5rem; padding: 0.8rem; display: flex; align-items: flex-start; gap: 0.8rem;&quot;&gt;
        &lt;div style=&quot;background-color: #faf5ff; width: 36px; height: 36px; display: flex; align-items: center; justify-content: center; border-radius: 0.3rem; color: #9333ea; font-weight: 800; font-size: 0.9rem; flex-shrink: 0;&quot;&gt;i,d&lt;/div&gt;
        &lt;div style=&quot;flex: 1; min-width: 0;&quot;&gt;
          &lt;div style=&quot;display: flex; align-items: center; gap: 0.4rem; margin-bottom: 0.3rem; white-space: nowrap; overflow: hidden;&quot;&gt;
            &lt;span style=&quot;font-weight: 800; font-size: 0.9rem; color: #1e293b;&quot;&gt;스토리지 최적화&lt;/span&gt;
            &lt;span style=&quot;font-size: 0.75rem; color: #64748b;&quot;&gt;&lpar;Storage&rpar;&lt;/span&gt;
            &lt;span style=&quot;font-size: 0.65rem; color: #6b21a8; background: #f3e8ff; padding: 0.1rem 0.3rem; border-radius: 3px; font-weight: 700;&quot;&gt;Hint: I/O, Data&lt;/span&gt;
          &lt;/div&gt;
          &lt;div style=&quot;font-size: 0.8rem; line-height: 1.6; color: #475569;&quot;&gt;
            높은 디스크 &lt;strong&gt;I/O 처리량&lt;/strong&gt; 필요
            &lt;span style=&quot;background:#f1f5f9; padding:0 0.3rem; border-radius:3px; color:#475569; margin-left:0.2rem;&quot;&gt;NoSQL/SQL DB&lt;/span&gt;
            &lt;span style=&quot;background:#f1f5f9; padding:0 0.3rem; border-radius:3px; color:#475569;&quot;&gt;트랜잭션&lt;/span&gt;
            &lt;span style=&quot;background:#f1f5f9; padding:0 0.3rem; border-radius:3px; color:#475569;&quot;&gt;DW&lt;/span&gt;
          &lt;/div&gt;
        &lt;/div&gt;
      &lt;/div&gt;

      &lt;div style=&quot;background-color: #fff; border: 1px solid #e2e8f0; border-radius: 0.5rem; padding: 0.8rem; display: flex; align-items: flex-start; gap: 0.8rem;&quot;&gt;
        &lt;div style=&quot;background-color: #ecfeff; width: 36px; height: 36px; display: flex; align-items: center; justify-content: center; border-radius: 0.3rem; color: #0891b2; font-weight: 800; font-size: 1.1rem; flex-shrink: 0;&quot;&gt;t&lt;/div&gt;
        &lt;div style=&quot;flex: 1; min-width: 0;&quot;&gt;
          &lt;div style=&quot;display: flex; align-items: center; gap: 0.4rem; margin-bottom: 0.3rem; white-space: nowrap; overflow: hidden;&quot;&gt;
            &lt;span style=&quot;font-weight: 800; font-size: 0.9rem; color: #1e293b;&quot;&gt;버스팅 퍼포먼스&lt;/span&gt;
            &lt;span style=&quot;font-size: 0.75rem; color: #64748b;&quot;&gt;&lpar;Burstable&rpar;&lt;/span&gt;
            &lt;span style=&quot;font-size: 0.65rem; color: #0e7490; background: #cffafe; padding: 0.1rem 0.3rem; border-radius: 3px; font-weight: 700;&quot;&gt;Hint: Turbo/Tiny&lt;/span&gt;
          &lt;/div&gt;
          &lt;div style=&quot;font-size: 0.8rem; line-height: 1.6; color: #475569;&quot;&gt;
            기본 성능 + 필요 시 &lt;strong&gt;버스트&lpar;가속&rpar;&lt;/strong&gt;
            &lt;span style=&quot;background:#f1f5f9; padding:0 0.3rem; border-radius:3px; color:#475569; margin-left:0.2rem;&quot;&gt;개발/테스트&lt;/span&gt;
            &lt;span style=&quot;background:#f1f5f9; padding:0 0.3rem; border-radius:3px; color:#475569;&quot;&gt;소규모 웹/DB&lt;/span&gt;
            &lt;span style=&quot;background:#f1f5f9; padding:0 0.3rem; border-radius:3px; color:#475569;&quot;&gt;마이크로서비스&lt;/span&gt;
          &lt;/div&gt;
        &lt;/div&gt;
      &lt;/div&gt;

    &lt;/div&gt;
  &lt;/div&gt;

&lt;/div&gt;

&lt;p class=&quot;story-box&quot;&gt;일반적으로 입문자가 프리티어로 접하는 &lt;strong&gt;t 시리즈&lt;/strong&gt;는 평소에는 적절한 성능을 유지하다가, 트래픽이 몰릴 때 일시적으로 성능을 높일 수 있어 비용 효율적입니다. 실제 서비스 성격에 맞춰 적절한 패밀리를 선택하는 것이 클라우드 비용 절감의 시작입니다.&lt;/p&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;h3 id=&quot;ec2-인스턴스-구매-옵션&quot;&gt;EC2 인스턴스 구매 옵션&lt;/h3&gt;

&lt;div class=&quot;story-box&quot;&gt;
  &lt;p&gt;EC2는 사용 목적과 기간에 따라 다양한 요금제를 제공합니다. 마치 호텔을 예약할 때 “하루만 묵을지”, “1년 회원권을 끊을지”, “땡처리 방을 잡을지” 고민하는 것과 비슷합니다.&lt;/p&gt;

  &lt;p&gt;가장 기본이 되는 두 가지 방식부터 살펴보겠습니다.&lt;/p&gt;
&lt;/div&gt;

&lt;h4 id=&quot;1-기본-구매-방식-단기유동적&quot;&gt;1. 기본 구매 방식 &lpar;단기/유동적&rpar;&lt;/h4&gt;

&lt;p class=&quot;story-box&quot;&gt;대부분의 입문자가 처음 접하는 방식입니다.&lt;/p&gt;

&lt;div class=&quot;info-box&quot;&gt;
&lt;div style=&quot;background-color: #f8fafc; padding: 1.5rem; border-radius: 0.75rem; border: 1px solid #e2e8f0; &quot;&gt;
  &lt;div style=&quot;display: grid; grid-template-columns: repeat&lpar;auto-fit, minmax&lpar;280px, 1fr&rpar;&rpar;; gap: 1rem;&quot;&gt;
    
    &lt;div style=&quot;background: white; border-radius: 0.5rem; border: 1px solid #e2e8f0; overflow: hidden; display: flex; flex-direction: column;&quot;&gt;
      &lt;div style=&quot;background: #3b82f6; padding: 0.8rem; color: white; display: flex; align-items: center; justify-content: space-between;&quot;&gt;
        &lt;span style=&quot;font-weight: 700;&quot;&gt;온디맨드 &lpar;On-Demand&rpar;&lt;/span&gt;
        &lt;i class=&quot;fas fa-clock&quot;&gt;&lt;/i&gt;
      &lt;/div&gt;
      &lt;div style=&quot;padding: 1rem; flex: 1; display: flex; flex-direction: column; justify-content: space-between;&quot;&gt;
        &lt;div&gt;
          &lt;div style=&quot;background: #eff6ff; border-radius: 0.3rem; padding: 0.5rem; margin-bottom: 0.8rem; font-size: 0.9rem; color: #1e3a8a; text-align: center;&quot;&gt;
            🏨 &lt;strong&gt;&quot;제값 내고 하루만 묵을게요&quot;&lt;/strong&gt;
          &lt;/div&gt;
          &lt;ul style=&quot;margin: 0; padding-left: 1.2rem; color: #475569; font-size: 0.85rem; line-height: 1.6;&quot;&gt;
            &lt;li&gt;가장 일반적인 요금제&lt;/li&gt;
            &lt;li&gt;초 단위 과금 &lpar;쓴 만큼만 냄&rpar;&lt;/li&gt;
            &lt;li&gt;약정 X, 선불 X&lt;/li&gt;
          &lt;/ul&gt;
        &lt;/div&gt;
        &lt;div style=&quot;margin-top: 1rem; text-align: center; font-size: 0.8rem; color: #64748b; background: #f1f5f9; padding: 0.3rem; border-radius: 4px;&quot;&gt;
           👉 &lt;strong&gt;개발, 테스트, 단기 작업&lt;/strong&gt; 추천
        &lt;/div&gt;
      &lt;/div&gt;
    &lt;/div&gt;

    &lt;div style=&quot;background: white; border-radius: 0.5rem; border: 1px solid #e2e8f0; overflow: hidden; display: flex; flex-direction: column;&quot;&gt;
      &lt;div style=&quot;background: #f97316; padding: 0.8rem; color: white; display: flex; align-items: center; justify-content: space-between;&quot;&gt;
        &lt;span style=&quot;font-weight: 700;&quot;&gt;스팟 &lpar;Spot&rpar;&lt;/span&gt;
        &lt;span style=&quot;background: #fff; color: #ea580c; font-size: 0.75rem; padding: 0.1rem 0.5rem; border-radius: 4px; font-weight: 800;&quot;&gt;최대 90% 할인&lt;/span&gt;
      &lt;/div&gt;
      &lt;div style=&quot;padding: 1rem; flex: 1; display: flex; flex-direction: column; justify-content: space-between;&quot;&gt;
        &lt;div&gt;
          &lt;div style=&quot;background: #fff7ed; border-radius: 0.3rem; padding: 0.5rem; margin-bottom: 0.8rem; font-size: 0.9rem; color: #9a3412; text-align: center;&quot;&gt;
            🏨 &lt;strong&gt;&quot;빈방 땡처리 경매&quot;&lt;/strong&gt;
          &lt;/div&gt;
          &lt;ul style=&quot;margin: 0; padding-left: 1.2rem; color: #475569; font-size: 0.85rem; line-height: 1.6;&quot;&gt;
            &lt;li&gt;AWS의 남는 자원을 싸게 이용&lt;/li&gt;
            &lt;li&gt;&lt;strong&gt;단, 더 비싼 입찰자가 오면 뺏김&lt;/strong&gt;&lt;/li&gt;
            &lt;li&gt;언제든 중단될 수 있음&lt;/li&gt;
          &lt;/ul&gt;
        &lt;/div&gt;
        &lt;div style=&quot;margin-top: 1rem; text-align: center; font-size: 0.8rem; color: #64748b; background: #f1f5f9; padding: 0.3rem; border-radius: 4px;&quot;&gt;
           👉 &lt;strong&gt;데이터 분석, 배치 처리&lt;/strong&gt;&lt;br /&gt;&lpar;중단돼도 괜찮은&rpar;
        &lt;/div&gt;
      &lt;/div&gt;
    &lt;/div&gt;

  &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;

&lt;h4 id=&quot;2-장기-약정-할인-1년--3년-계약&quot;&gt;2. 장기 약정 할인 &lpar;1년 / 3년 계약&rpar;&lt;/h4&gt;

&lt;p class=&quot;story-box&quot;&gt;서비스를 장기적으로 운영할 계획이라면, 미리 약정을 걸어 비용을 크게 아낄 수 있습니다. AWS는 최근 &lt;strong&gt;Savings Plans&lt;/strong&gt;를 강력하게 권장하는 추세입니다.&lt;/p&gt;

&lt;div class=&quot;info-box&quot;&gt;
  &lt;div style=&quot;background-color: #f8fafc; padding: 1.5rem; border-radius: 0.75rem; border: 1px solid #e2e8f0; &quot;&gt;
  
  &lt;div style=&quot;text-align: center; margin-bottom: 1.5rem;&quot;&gt;
    &lt;span style=&quot;background: #0f172a; color: white; padding: 0.4rem 1rem; border-radius: 99px; font-size: 0.9rem; font-weight: 700;&quot;&gt;
      &lt;i class=&quot;fas fa-handshake&quot; style=&quot;margin-right: 0.3rem;&quot;&gt;&lt;/i&gt; 최대 72% 할인
    &lt;/span&gt;
    &lt;p style=&quot;margin-top: 0.5rem; color: #64748b; font-size: 0.9rem;&quot;&gt;
      &quot;1년/3년 동안 꾸준히 쓸 테니 깎아주세요&quot; &lpar;전체 선불 시 할인율 최대&rpar;
    &lt;/p&gt;
  &lt;/div&gt;

  &lt;div style=&quot;display: flex; gap: 1rem; flex-wrap: wrap; margin-bottom: 1.5rem;&quot;&gt;
    &lt;div style=&quot;flex: 1; min-width: 280px; background: white; border: 1px solid #cbd5e1; border-radius: 0.5rem; overflow: hidden;&quot;&gt;
      &lt;div style=&quot;background: #eff6ff; color: #1e40af; padding: 0.6rem; text-align: center; font-weight: 700; border-bottom: 1px solid #bfdbfe;&quot;&gt;
        1. 예약 인스턴스 &lpar;RI&rpar;
      &lt;/div&gt;
      &lt;div style=&quot;padding: 1rem;&quot;&gt;
        &lt;p style=&quot;font-size: 0.85rem; color: #475569; margin-bottom: 0.8rem; text-align: center;&quot;&gt;
          특정 &lt;strong&gt;기기 자체&lt;/strong&gt;를 예약
        &lt;/p&gt;
        &lt;div style=&quot;background: #f1f5f9; padding: 0.5rem; border-radius: 4px; font-size: 0.8rem; color: #334155; margin-bottom: 0.5rem;&quot;&gt;
          &lt;strong&gt;• 표준 &lpar;Standard&rpar;:&lt;/strong&gt; 변경 불가 / 할인율 높음 &lpar;72%&rpar;
        &lt;/div&gt;
        &lt;div style=&quot;background: #fff; border: 1px solid #e2e8f0; padding: 0.5rem; border-radius: 4px; font-size: 0.8rem; color: #334155;&quot;&gt;
          &lt;strong&gt;• 전환형 &lpar;Convertible&rpar;:&lt;/strong&gt; 패밀리, OS 변경 가능 / 할인율 낮음 &lpar;66%&rpar;
        &lt;/div&gt;
      &lt;/div&gt;
    &lt;/div&gt;

    &lt;div style=&quot;flex: 1; min-width: 280px; background: white; border: 2px solid #34d399; border-radius: 0.5rem; overflow: hidden; position: relative;&quot;&gt;
      &lt;div style=&quot;position: absolute; top: 0; right: 0; background: #34d399; color: white; font-size: 0.7rem; font-weight: 800; padding: 0.2rem 0.5rem; border-bottom-left-radius: 6px;&quot;&gt;추천 ✨&lt;/div&gt;
      &lt;div style=&quot;background: #ecfdf5; color: #065f46; padding: 0.6rem; text-align: center; font-weight: 700; border-bottom: 1px solid #6ee7b7;&quot;&gt;
        2. Savings Plans &lpar;SP&rpar;
      &lt;/div&gt;
      &lt;div style=&quot;padding: 1rem;&quot;&gt;
        &lt;p style=&quot;font-size: 0.85rem; color: #475569; margin-bottom: 0.8rem; text-align: center;&quot;&gt;
          시간당 &lt;strong&gt;약정 금액&lpar;$descriptionrpar;&lt;/strong&gt;을 채우면 됨
        &lt;/p&gt;
        &lt;div style=&quot;background: #f1f5f9; padding: 0.5rem; border-radius: 4px; font-size: 0.8rem; color: #334155; margin-bottom: 0.5rem;&quot;&gt;
          &lt;strong&gt;• EC2 SP:&lt;/strong&gt; 특정 패밀리/리전 고정 &lpar;최대 72%&rpar;
        &lt;/div&gt;
        &lt;div style=&quot;background: #d1fae5; border: 1px solid #34d399; padding: 0.5rem; border-radius: 4px; font-size: 0.8rem; color: #064e3b; font-weight: 700;&quot;&gt;
          • Compute SP: EC2 + Fargate + Lambda + SageMaker ✅
        &lt;/div&gt;
      &lt;/div&gt;
    &lt;/div&gt;
  &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;

&lt;div class=&quot;story-box&quot;&gt;
  &lt;p&gt;&lt;strong&gt;💡 어떤 Savings Plan을 선택해야 할까요?&lt;/strong&gt;&lt;/p&gt;

  &lt;ul&gt;
    &lt;li&gt;&lt;strong&gt;EC2만&lt;/strong&gt; 사용하고, &lt;strong&gt;리전/패밀리 변경 계획이 없다&lt;/strong&gt; &lt;i class=&quot;fas fa-arrow-right&quot; style=&quot;font-size:0.7rem; margin:0 5px;&quot;&gt;&lt;/i&gt; &lt;strong&gt;EC2 Instance SP&lt;/strong&gt; &lpar;할인율 ⬆️&rpar;&lt;/li&gt;
    &lt;li&gt;&lt;strong&gt;Lambda, Fargate&lt;/strong&gt; 등을 섞어 쓰거나, &lt;strong&gt;인스턴스 유형을 자주 바꾼다&lt;/strong&gt; &lt;i class=&quot;fas fa-arrow-right&quot; style=&quot;font-size:0.7rem; margin:0 5px;&quot;&gt;&lt;/i&gt; &lt;strong&gt;Compute SP&lt;/strong&gt; &lpar;유연성 ⬆️&rpar;&lt;/li&gt;
  &lt;/ul&gt;
&lt;/div&gt;

&lt;h4 id=&quot;3-특수-목적-규제-및-라이선스&quot;&gt;3. 특수 목적 &lpar;규제 및 라이선스&rpar;&lt;/h4&gt;

&lt;p class=&quot;story-box&quot;&gt;보안 규정이나 라이선스 문제로 하드웨어를 단독으로 써야 할 때 사용하는 옵션입니다.&lt;/p&gt;

&lt;div class=&quot;info-box&quot;&gt;
&lt;div style=&quot;max-width: 800px; margin: 0 auto; background-color: #f8fafc; padding: 1.5rem; border-radius: 0.75rem; border: 1px solid #e2e8f0; margin-bottom: 2rem;&quot;&gt;
  
  &lt;div style=&quot;display: grid; grid-template-columns: repeat&lpar;3, 1fr&rpar;; gap: 0.8rem; margin-bottom: 2rem;&quot;&gt;
    
    &lt;div style=&quot;background: white; padding: 0.8rem; border-radius: 0.5rem; border: 1px solid #e2e8f0; display: flex; flex-direction: column;&quot;&gt;
      &lt;div style=&quot;margin-bottom: 0.5rem; text-align: center;&quot;&gt;
        &lt;strong style=&quot;font-size: 0.9rem; color: #1e293b;&quot;&gt;🏢 전용 호스트&lt;br /&gt;&lt;span style=&quot;font-size: 0.75rem; color: #64748b;&quot;&gt;&lpar;Dedicated Host&rpar;&lt;/span&gt;&lt;/strong&gt;
      &lt;/div&gt;
      &lt;div style=&quot;background: #eff6ff; padding: 0.5rem; border-radius: 4px; color: #1e40af; font-size: 0.8rem; margin-bottom: 0.8rem; text-align: center; font-weight: 700; height: 100%; display: flex; align-items: center; justify-content: center;&quot;&gt;
        &quot;건물 통째로 매입&quot;
      &lt;/div&gt;
      &lt;div style=&quot;font-size: 0.75rem; color: #475569; line-height: 1.5; text-align: center;&quot;&gt;
        물리 서버 제어권 보유&lt;br /&gt;
        &lt;span style=&quot;color: #dc2626; font-weight: 700;&quot;&gt;가장 비쌈&lt;/span&gt;
      &lt;/div&gt;
    &lt;/div&gt;

    &lt;div style=&quot;background: white; padding: 0.8rem; border-radius: 0.5rem; border: 1px solid #e2e8f0; display: flex; flex-direction: column;&quot;&gt;
      &lt;div style=&quot;margin-bottom: 0.5rem; text-align: center;&quot;&gt;
        &lt;strong style=&quot;font-size: 0.9rem; color: #1e293b;&quot;&gt;🔒 전용 인스턴스&lt;br /&gt;&lt;span style=&quot;font-size: 0.75rem; color: #64748b;&quot;&gt;&lpar;Dedicated Instance&rpar;&lt;/span&gt;&lt;/strong&gt;
      &lt;/div&gt;
      &lt;div style=&quot;background: #f0fdf4; padding: 0.5rem; border-radius: 4px; color: #166534; font-size: 0.8rem; margin-bottom: 0.8rem; text-align: center; font-weight: 700; height: 100%; display: flex; align-items: center; justify-content: center;&quot;&gt;
        &quot;전용 층 사용&quot;
      &lt;/div&gt;
      &lt;div style=&quot;font-size: 0.75rem; color: #475569; line-height: 1.5; text-align: center;&quot;&gt;
        하드웨어 격리 보장&lt;br /&gt;
        &lt;span style=&quot;color: #64748b;&quot;&gt;배치 제어 불가&lt;/span&gt;
      &lt;/div&gt;
    &lt;/div&gt;

    &lt;div style=&quot;background: white; padding: 0.8rem; border-radius: 0.5rem; border: 1px solid #e2e8f0; display: flex; flex-direction: column;&quot;&gt;
      &lt;div style=&quot;margin-bottom: 0.5rem; text-align: center;&quot;&gt;
        &lt;strong style=&quot;font-size: 0.9rem; color: #1e293b;&quot;&gt;📅 용량 예약&lt;br /&gt;&lt;span style=&quot;font-size: 0.75rem; color: #64748b;&quot;&gt;&lpar;Capacity Res.&rpar;&lt;/span&gt;&lt;/strong&gt;
      &lt;/div&gt;
      &lt;div style=&quot;background: #fff7ed; padding: 0.5rem; border-radius: 4px; color: #9a3412; font-size: 0.8rem; margin-bottom: 0.8rem; text-align: center; font-weight: 700; height: 100%; display: flex; align-items: center; justify-content: center;&quot;&gt;
        &quot;자리 미리 찜&quot;
      &lt;/div&gt;
      &lt;div style=&quot;font-size: 0.75rem; color: #475569; line-height: 1.5; text-align: center;&quot;&gt;
        확실한 인스턴스 확보&lt;br /&gt;
        &lt;span style=&quot;color: #ea580c; font-weight: 700;&quot;&gt;미사용 시에도 과금&lt;/span&gt;
      &lt;/div&gt;
    &lt;/div&gt;

  &lt;/div&gt;

  &lt;div style=&quot;background: white; border-radius: 0.5rem; border: 1px solid #cbd5e1; overflow: hidden; width: 100%; box-sizing: border-box;&quot;&gt;
    &lt;div style=&quot;background: #334155; color: white; padding: 0.6rem; text-align: center; font-size: 0.9rem; font-weight: 700;&quot;&gt;
      📝 한눈에 외우기 &lpar;Cheat Sheet&rpar;
    &lt;/div&gt;
    &lt;div style=&quot;overflow-x: auto; width: 100%;&quot;&gt;
      &lt;table style=&quot;width: 100%; min-width: 600px; border-collapse: collapse; font-size: 0.8rem; text-align: center; table-layout: fixed;&quot;&gt;
        &lt;thead&gt;
          &lt;tr style=&quot;background: #f1f5f9; color: #475569;&quot;&gt;
            &lt;th style=&quot;padding: 0.6rem; border-bottom: 2px solid #e2e8f0; width: 20%;&quot;&gt;구분&lt;/th&gt;
            &lt;th style=&quot;padding: 0.6rem; border-bottom: 2px solid #e2e8f0; width: 26.6%;&quot;&gt;전용 호스트&lt;br /&gt;&lpar;Host&rpar;&lt;/th&gt;
            &lt;th style=&quot;padding: 0.6rem; border-bottom: 2px solid #e2e8f0; width: 26.6%;&quot;&gt;전용 인스턴스&lt;br /&gt;&lpar;Instance&rpar;&lt;/th&gt;
            &lt;th style=&quot;padding: 0.6rem; border-bottom: 2px solid #e2e8f0; width: 26.6%;&quot;&gt;용량 예약&lt;br /&gt;&lpar;Capacity&rpar;&lt;/th&gt;
          &lt;/tr&gt;
        &lt;/thead&gt;
        &lt;tbody style=&quot;color: #334155;&quot;&gt;
          &lt;tr&gt;
            &lt;td style=&quot;padding: 0.6rem; border-bottom: 1px solid #e2e8f0; font-weight: 700; background: #f8fafc; word-break: keep-all;&quot;&gt;
              하드웨어 공유
            &lt;/td&gt;
            &lt;td style=&quot;padding: 0.6rem; border-bottom: 1px solid #e2e8f0; color: #dc2626; font-weight: 700;&quot;&gt;X&lt;/td&gt;
            &lt;td style=&quot;padding: 0.6rem; border-bottom: 1px solid #e2e8f0; color: #dc2626; font-weight: 700;&quot;&gt;X&lt;/td&gt;
            &lt;td style=&quot;padding: 0.6rem; border-bottom: 1px solid #e2e8f0; color: #64748b;&quot;&gt;&lpar;상관없음&rpar;&lt;/td&gt;
          &lt;/tr&gt;
          &lt;tr&gt;
            &lt;td style=&quot;padding: 0.6rem; border-bottom: 1px solid #e2e8f0; font-weight: 700; background: #f8fafc; word-break: keep-all;&quot;&gt;
              배치 제어&lt;br /&gt;&lt;span style=&quot;font-weight:400; font-size:0.7em&quot;&gt;&lpar;Placement&rpar;&lt;/span&gt;
            &lt;/td&gt;
            &lt;td style=&quot;padding: 0.6rem; border-bottom: 1px solid #e2e8f0;&quot;&gt;
              &lt;span style=&quot;background: #dcfce7; color: #166534; padding: 0.1rem 0.4rem; border-radius: 99px; font-weight: 700; display: inline-block;&quot;&gt;가능 &lpar;O&rpar;&lt;/span&gt;
            &lt;/td&gt;
            &lt;td style=&quot;padding: 0.6rem; border-bottom: 1px solid #e2e8f0; color: #94a3b8;&quot;&gt;
              불가능 &lpar;X&rpar;
            &lt;/td&gt;
            &lt;td style=&quot;padding: 0.6rem; border-bottom: 1px solid #e2e8f0; color: #94a3b8;&quot;&gt;
              -
            &lt;/td&gt;
          &lt;/tr&gt;
          &lt;tr&gt;
            &lt;td style=&quot;padding: 0.6rem; border-bottom: 1px solid #e2e8f0; font-weight: 700; background: #f8fafc; word-break: keep-all;&quot;&gt;
              라이선스&lpar;BYOL&rpar;&lt;br /&gt;&lt;span style=&quot;font-weight:400; font-size:0.7em&quot;&gt;&lpar;Compliance&rpar;&lt;/span&gt;
            &lt;/td&gt;
            &lt;td style=&quot;padding: 0.6rem; border-bottom: 1px solid #e2e8f0;&quot;&gt;
              &lt;span style=&quot;background: #dcfce7; color: #166534; padding: 0.1rem 0.4rem; border-radius: 99px; font-weight: 700; display: inline-block;&quot;&gt;가능 &lpar;O&rpar;&lt;/span&gt;
            &lt;/td&gt;
            &lt;td style=&quot;padding: 0.6rem; border-bottom: 1px solid #e2e8f0; color: #94a3b8;&quot;&gt;
              불가능 &lpar;X&rpar;
            &lt;/td&gt;
            &lt;td style=&quot;padding: 0.6rem; border-bottom: 1px solid #e2e8f0; color: #94a3b8;&quot;&gt;
              -
            &lt;/td&gt;
          &lt;/tr&gt;
          &lt;tr&gt;
            &lt;td style=&quot;padding: 0.6rem; font-weight: 700; background: #f8fafc; word-break: keep-all;&quot;&gt;
              과금/약정 특징
            &lt;/td&gt;
            &lt;td style=&quot;padding: 0.6rem; font-size: 0.75rem; word-break: keep-all;&quot;&gt;
              서버 단위 과금
            &lt;/td&gt;
            &lt;td style=&quot;padding: 0.6rem; font-size: 0.75rem; word-break: keep-all;&quot;&gt;
              인스턴스 과금&lt;br /&gt;&lpar;+$2/Region&rpar;
            &lt;/td&gt;
            &lt;td style=&quot;padding: 0.6rem; font-size: 0.75rem; word-break: keep-all;&quot;&gt;
              시간 약정 없음&lt;br /&gt;&lpar;단기 사용 가능&rpar;
            &lt;/td&gt;
          &lt;/tr&gt;
        &lt;/tbody&gt;
      &lt;/table&gt;
    &lt;/div&gt;
  &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;

&lt;div style=&quot;margin-bottom: 1.5rem; &quot;&gt;
    &lt;h4 style=&quot;margin: 0; color: #1e293b;font-weight: 800;&quot;&gt;✔️ 놓치기 쉬운 핵심 디테일 3가지 &lpar;Deep Dive&rpar;&lt;/h4&gt;
  &lt;/div&gt;

&lt;div class=&quot;deep-dive-list&quot;&gt;

    &lt;div class=&quot;dd-item&quot;&gt;
      &lt;div class=&quot;dd-header&quot;&gt;
        &lt;span class=&quot;dd-title&quot;&gt;1. 전용 인스턴스: 배치가 바뀐다?&lt;/span&gt;
        &lt;span class=&quot;dd-badge red&quot;&gt;함정 주의&lt;/span&gt;
      &lt;/div&gt;
      &lt;p class=&quot;dd-content&quot;&gt;
        &quot;나만 쓰는 하드웨어&quot;는 맞지만, &lt;span class=&quot;code-span&quot;&gt;중지&lpar;Stop&rpar; 후 시작&lpar;Start&rpar;&lt;/span&gt;하면 다른 기계로 이사 갈 수 있습니다.
        &lt;span class=&quot;sub-text&quot;&gt;👉 따라서 &lt;strong&gt;배치 제어&lpar;Placement Control&rpar;&lt;/strong&gt;가 불가능합니다. &lpar;원하는 랙에 고정 불가&rpar;&lt;/span&gt;
      &lt;/p&gt;
    &lt;/div&gt;

    &lt;div class=&quot;dd-item&quot;&gt;
      &lt;div class=&quot;dd-header&quot;&gt;
        &lt;span class=&quot;dd-title&quot;&gt;2. 용량 예약 + 할인 조합법&lt;/span&gt;
        &lt;span class=&quot;dd-badge blue&quot;&gt;Tip&lt;/span&gt;
      &lt;/div&gt;
      &lt;p class=&quot;dd-content&quot;&gt;
        용량 예약 자체는 &lt;span class=&quot;code-span&quot;&gt;할인 0% &lpar;정가&rpar;&lt;/span&gt;입니다. 하지만 다른 할인과 합체가 가능합니다.
        &lt;span class=&quot;sub-text highlight-box&quot;&gt;🎯 &lpar;용량 예약으로 자리 확보&rpar; + &lpar;RI/SP로 요금 할인&rpar; = 완벽 조합&lt;/span&gt;
      &lt;/p&gt;
    &lt;/div&gt;

    &lt;div class=&quot;dd-item&quot;&gt;
      &lt;div class=&quot;dd-header&quot;&gt;
        &lt;span class=&quot;dd-title&quot;&gt;3. 전용 호스트: 내 라이선스 쓰기&lpar;BYOL&rpar;&lt;/span&gt;
      &lt;/div&gt;
      &lt;p class=&quot;dd-content&quot;&gt;
        물리 서버 전체를 점유하므로 기존 온프레미스에서 쓰던 기업용 라이선스를 그대로 가져올 수 있습니다.
        &lt;span class=&quot;sub-text&quot;&gt;👉 기준: &lt;strong&gt;소켓&lpar;Socket&rpar;당, 코어&lpar;Core&rpar;당, VM당&lt;/strong&gt; 라이선스&lt;/span&gt;
      &lt;/p&gt;
    &lt;/div&gt;

  &lt;/div&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;h3 id=&quot;배치-그룹-전략placement-groups&quot;&gt;배치 그룹 전략&lpar;Placement Groups&rpar;&lt;/h3&gt;

&lt;p class=&quot;story-box&quot;&gt;인스턴스 물리적 배치 전략&lt;/p&gt;

&lt;div class=&quot;info-box&quot;&gt;

&lt;div style=&quot;padding:0 1rem; border-radius: 0.75rem; font-size: 0.85rem; letter-spacing: -0.03em;&quot;&gt;

  &lt;div style=&quot;display: grid; grid-template-columns: repeat&lpar;3, 1fr&rpar;; gap: 1rem;&quot;&gt;

    &lt;div style=&quot;background: white; border: 1px solid #e9d5ff; border-radius: 0.5rem; overflow: hidden; display: flex; flex-direction: column;&quot;&gt;
      &lt;div style=&quot;background: #faf5ff; padding: 0.6rem; border-bottom: 1px solid #e9d5ff; text-align: center;&quot;&gt;
        &lt;i class=&quot;fas fa-th-large&quot; style=&quot;color: #9333ea; font-size: 1.2rem; margin-bottom: 0.3rem;&quot;&gt;&lt;/i&gt;
        &lt;div style=&quot;font-weight: 800; color: #6b21a8; font-size: 0.95rem;&quot;&gt;클러스터 &lpar;Cluster&rpar;&lt;/div&gt;
        &lt;span style=&quot;font-size: 0.7rem; color: #7e22ce; background: #e9d5ff; padding: 0.1rem 0.4rem; border-radius: 3px; font-weight: 700;&quot;&gt;단일 AZ / 초고속&lt;/span&gt;
      &lt;/div&gt;

      &lt;div style=&quot;padding: 0.8rem; background: #fff; display: flex; justify-content: center; border-bottom: 1px dashed #f3e8ff;&quot;&gt;
        &lt;div style=&quot;border: 2px solid #d8b4fe; border-radius: 6px; padding: 6px; background-color: #faf5ff;&quot;&gt;
          &lt;div style=&quot;font-size: 0.6rem; color: #a855f7; text-align: center; margin-bottom: 2px; font-weight: 700;&quot;&gt;Rack 1&lt;/div&gt;
          &lt;div style=&quot;display: grid; grid-template-columns: repeat&lpar;4, 1fr&rpar;; gap: 2px;&quot;&gt;
            &lt;div style=&quot;width: 10px; height: 10px; background: #a855f7; border-radius: 2px;&quot;&gt;&lt;/div&gt;
            &lt;div style=&quot;width: 10px; height: 10px; background: #a855f7; border-radius: 2px;&quot;&gt;&lt;/div&gt;
            &lt;div style=&quot;width: 10px; height: 10px; background: #a855f7; border-radius: 2px;&quot;&gt;&lt;/div&gt;
            &lt;div style=&quot;width: 10px; height: 10px; background: #a855f7; border-radius: 2px;&quot;&gt;&lt;/div&gt;
            &lt;div style=&quot;width: 10px; height: 10px; background: #a855f7; border-radius: 2px;&quot;&gt;&lt;/div&gt;
            &lt;div style=&quot;width: 10px; height: 10px; background: #a855f7; border-radius: 2px;&quot;&gt;&lt;/div&gt;
            &lt;div style=&quot;width: 10px; height: 10px; background: #a855f7; border-radius: 2px;&quot;&gt;&lt;/div&gt;
            &lt;div style=&quot;width: 10px; height: 10px; background: #a855f7; border-radius: 2px;&quot;&gt;&lt;/div&gt;
            &lt;div style=&quot;width: 10px; height: 10px; background: #a855f7; border-radius: 2px;&quot;&gt;&lt;/div&gt;
            &lt;div style=&quot;width: 10px; height: 10px; background: #a855f7; border-radius: 2px;&quot;&gt;&lt;/div&gt;
            &lt;div style=&quot;width: 10px; height: 10px; background: #a855f7; border-radius: 2px;&quot;&gt;&lt;/div&gt;
            &lt;div style=&quot;width: 10px; height: 10px; background: #a855f7; border-radius: 2px;&quot;&gt;&lt;/div&gt;
            &lt;div style=&quot;width: 10px; height: 10px; background: #a855f7; border-radius: 2px;&quot;&gt;&lt;/div&gt;
            &lt;div style=&quot;width: 10px; height: 10px; background: #a855f7; border-radius: 2px;&quot;&gt;&lt;/div&gt;
            &lt;div style=&quot;width: 10px; height: 10px; background: #a855f7; border-radius: 2px;&quot;&gt;&lt;/div&gt;
            &lt;div style=&quot;width: 10px; height: 10px; background: #a855f7; border-radius: 2px;&quot;&gt;&lt;/div&gt;
          &lt;/div&gt;
        &lt;/div&gt;
      &lt;/div&gt;

      &lt;div style=&quot;padding: 0.6rem; flex: 1; display: flex; flex-direction: column; justify-content: space-between;&quot;&gt;
        &lt;ul style=&quot;margin: 0; padding-left: 0.8rem; color: #475569; line-height: 1.4; font-size: 0.8rem; margin-bottom: 0.5rem;&quot;&gt;
          &lt;li&gt;단일 AZ 내 인스턴스를 &lt;strong&gt;밀집&lpar;뭉침&rpar;&lt;/strong&gt;시켜 지연 시간 최소화&lt;/li&gt;
        &lt;/ul&gt;
        &lt;div style=&quot;background: #f3f4f6; border-radius: 0.3rem; padding: 0.4rem;&quot;&gt;
          &lt;strong style=&quot;color: #4b5563; font-size: 0.75rem; display: block; margin-bottom: 0.2rem;&quot;&gt;📌 용도&lt;/strong&gt;
          &lt;p style=&quot;margin: 0; font-size: 0.75rem; color: #64748b; line-height: 1.3;&quot;&gt;
            HPC, 머신러닝 등 노드 간 통신 속도가 중요한 작업
          &lt;/p&gt;
        &lt;/div&gt;
      &lt;/div&gt;
    &lt;/div&gt;

    &lt;div style=&quot;background: white; border: 1px solid #fed7aa; border-radius: 0.5rem; overflow: hidden; display: flex; flex-direction: column;&quot;&gt;
      &lt;div style=&quot;background: #fff7ed; padding: 0.6rem; border-bottom: 1px solid #fed7aa; text-align: center;&quot;&gt;
        &lt;i class=&quot;fas fa-arrows-alt-h&quot; style=&quot;color: #ea580c; font-size: 1.2rem; margin-bottom: 0.3rem;&quot;&gt;&lt;/i&gt;
        &lt;div style=&quot;font-weight: 800; color: #9a3412; font-size: 0.95rem;&quot;&gt;분산 &lpar;Spread&rpar;&lt;/div&gt;
        &lt;span style=&quot;font-size: 0.7rem; color: #c2410c; background: #ffedd5; padding: 0.1rem 0.4rem; border-radius: 3px; font-weight: 700;&quot;&gt;하드웨어 분리 / 안전&lt;/span&gt;
      &lt;/div&gt;

      &lt;div style=&quot;padding: 0.8rem; background: #fff; display: flex; justify-content: center; gap: 0.5rem; border-bottom: 1px dashed #ffedd5;&quot;&gt;
        &lt;div style=&quot;border: 2px solid #fdba74; border-radius: 4px; padding: 4px; width: 20px; display: flex; flex-direction: column; align-items: center; justify-content: center; height: 50px; background: #fff7ed;&quot;&gt;
          &lt;div style=&quot;width: 12px; height: 12px; background: #f97316; border-radius: 2px;&quot;&gt;&lt;/div&gt;
          &lt;span style=&quot;font-size: 0.5rem; color: #f97316; margin-top: auto;&quot;&gt;R1&lt;/span&gt;
        &lt;/div&gt;
        &lt;div style=&quot;border: 2px solid #fdba74; border-radius: 4px; padding: 4px; width: 20px; display: flex; flex-direction: column; align-items: center; justify-content: center; height: 50px; background: #fff7ed;&quot;&gt;
          &lt;div style=&quot;width: 12px; height: 12px; background: #f97316; border-radius: 2px;&quot;&gt;&lt;/div&gt;
          &lt;span style=&quot;font-size: 0.5rem; color: #f97316; margin-top: auto;&quot;&gt;R2&lt;/span&gt;
        &lt;/div&gt;
        &lt;div style=&quot;border: 2px solid #fdba74; border-radius: 4px; padding: 4px; width: 20px; display: flex; flex-direction: column; align-items: center; justify-content: center; height: 50px; background: #fff7ed;&quot;&gt;
          &lt;div style=&quot;width: 12px; height: 12px; background: #f97316; border-radius: 2px;&quot;&gt;&lt;/div&gt;
          &lt;span style=&quot;font-size: 0.5rem; color: #f97316; margin-top: auto;&quot;&gt;R3&lt;/span&gt;
        &lt;/div&gt;
      &lt;/div&gt;

      &lt;div style=&quot;padding: 0.6rem; flex: 1; display: flex; flex-direction: column; justify-content: space-between;&quot;&gt;
        &lt;ul style=&quot;margin: 0; padding-left: 0.8rem; color: #475569; line-height: 1.4; font-size: 0.8rem; margin-bottom: 0.5rem;&quot;&gt;
          &lt;li style=&quot;margin-bottom: 0.3rem;&quot;&gt;각 인스턴스를 &lt;strong&gt;서로 다른 하드웨어&lpar;Rack&rpar;&lt;/strong&gt;에 배치&lt;/li&gt;
          &lt;li&gt;AZ당 &lt;strong&gt;최대 7개&lt;/strong&gt; 제한&lt;/li&gt;
        &lt;/ul&gt;
        &lt;div style=&quot;background: #f3f4f6; border-radius: 0.3rem; padding: 0.4rem;&quot;&gt;
          &lt;strong style=&quot;color: #4b5563; font-size: 0.75rem; display: block; margin-bottom: 0.2rem;&quot;&gt;📌 특징&lt;/strong&gt;
          &lt;p style=&quot;margin: 0; font-size: 0.75rem; color: #64748b; line-height: 1.3;&quot;&gt;
            하드웨어 장애 시 다른 인스턴스 영향 X &lpar;격리&rpar;
          &lt;/p&gt;
        &lt;/div&gt;
      &lt;/div&gt;
    &lt;/div&gt;

    &lt;div style=&quot;background: white; border: 1px solid #bbf7d0; border-radius: 0.5rem; overflow: hidden; display: flex; flex-direction: column;&quot;&gt;
      &lt;div style=&quot;background: #f0fdf4; padding: 0.6rem; border-bottom: 1px solid #bbf7d0; text-align: center;&quot;&gt;
        &lt;i class=&quot;fas fa-layer-group&quot; style=&quot;color: #16a34a; font-size: 1.2rem; margin-bottom: 0.3rem;&quot;&gt;&lt;/i&gt;
        &lt;div style=&quot;font-weight: 800; color: #166534; font-size: 0.95rem;&quot;&gt;파티션 &lpar;Partition&rpar;&lt;/div&gt;
        &lt;span style=&quot;font-size: 0.7rem; color: #15803d; background: #dcfce7; padding: 0.1rem 0.4rem; border-radius: 3px; font-weight: 700;&quot;&gt;대규모 분산 / 빅데이터&lt;/span&gt;
      &lt;/div&gt;

      &lt;div style=&quot;padding: 0.8rem; background: #fff; display: flex; justify-content: center; gap: 0.3rem; border-bottom: 1px dashed #bbf7d0;&quot;&gt;
        &lt;div style=&quot;border: 1px dashed #86efac; border-radius: 4px; padding: 3px; background: #f0fdf4;&quot;&gt;
          &lt;div style=&quot;font-size: 0.5rem; color: #16a34a; text-align: center; margin-bottom: 2px;&quot;&gt;Partition 1&lt;/div&gt;
          &lt;div style=&quot;display: flex; gap: 2px;&quot;&gt;
             &lt;div style=&quot;border: 1px solid #86efac; padding: 1px; width: 14px; display: flex; flex-direction: column; align-items: center; gap: 1px;&quot;&gt;
                &lt;div style=&quot;width: 8px; height: 8px; background: #22c55e; border-radius: 1px;&quot;&gt;&lt;/div&gt;
                &lt;div style=&quot;width: 8px; height: 8px; background: #22c55e; border-radius: 1px;&quot;&gt;&lt;/div&gt;
             &lt;/div&gt;
             &lt;div style=&quot;border: 1px solid #86efac; padding: 1px; width: 14px; display: flex; flex-direction: column; align-items: center; gap: 1px;&quot;&gt;
                &lt;div style=&quot;width: 8px; height: 8px; background: #22c55e; border-radius: 1px;&quot;&gt;&lt;/div&gt;
             &lt;/div&gt;
          &lt;/div&gt;
        &lt;/div&gt;
        &lt;div style=&quot;border: 1px dashed #86efac; border-radius: 4px; padding: 3px; background: #f0fdf4;&quot;&gt;
          &lt;div style=&quot;font-size: 0.5rem; color: #16a34a; text-align: center; margin-bottom: 2px;&quot;&gt;Partition 2&lt;/div&gt;
          &lt;div style=&quot;display: flex; gap: 2px;&quot;&gt;
             &lt;div style=&quot;border: 1px solid #86efac; padding: 1px; width: 14px; display: flex; flex-direction: column; align-items: center; gap: 1px;&quot;&gt;
                &lt;div style=&quot;width: 8px; height: 8px; background: #22c55e; border-radius: 1px;&quot;&gt;&lt;/div&gt;
             &lt;/div&gt;
             &lt;div style=&quot;border: 1px solid #86efac; padding: 1px; width: 14px; display: flex; flex-direction: column; align-items: center; gap: 1px;&quot;&gt;
                &lt;div style=&quot;width: 8px; height: 8px; background: #22c55e; border-radius: 1px;&quot;&gt;&lt;/div&gt;
                &lt;div style=&quot;width: 8px; height: 8px; background: #22c55e; border-radius: 1px;&quot;&gt;&lt;/div&gt;
             &lt;/div&gt;
          &lt;/div&gt;
        &lt;/div&gt;
      &lt;/div&gt;

      &lt;div style=&quot;padding: 0.6rem; flex: 1; display: flex; flex-direction: column; justify-content: space-between;&quot;&gt;
        &lt;ul style=&quot;margin: 0; padding-left: 0.8rem; color: #475569; line-height: 1.4; font-size: 0.8rem; margin-bottom: 0.5rem;&quot;&gt;
          &lt;li&gt;파티션&lpar;랙 집합&rpar; 단위로 분산하여 하드웨어 공유 X&lt;/li&gt;
          &lt;li&gt;단일 AZ 내 &lt;strong&gt;수백 개 EC2&lt;/strong&gt; 확장&lt;/li&gt;
        &lt;/ul&gt;
        &lt;div style=&quot;background: #f3f4f6; border-radius: 0.3rem; padding: 0.4rem;&quot;&gt;
          &lt;strong style=&quot;color: #4b5563; font-size: 0.75rem; display: block; margin-bottom: 0.2rem;&quot;&gt;📌 적합한 작업&lt;/strong&gt;
          &lt;p style=&quot;margin: 0; font-size: 0.75rem; color: #64748b; line-height: 1.3;&quot;&gt;
            Hadoop, Kafka, Cassandra &lpar;분산 처리&rpar;
          &lt;/p&gt;
        &lt;/div&gt;
      &lt;/div&gt;
    &lt;/div&gt;

  &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;

&lt;div style=&quot;margin-bottom: 1.5rem;&quot;&gt;
  &lt;h4 style=&quot;margin: 0; color: #1e293b; font-weight: 800;&quot;&gt;✔️ 배치 그룹 선택 가이드 &lpar;Deep Dive&rpar;&lt;/h4&gt;
&lt;/div&gt;

&lt;div class=&quot;deep-dive-list&quot;&gt;

  &lt;div class=&quot;dd-item&quot;&gt;
    &lt;div class=&quot;dd-header&quot;&gt;
      &lt;span class=&quot;dd-title&quot;&gt;1. 클러스터&lpar;Cluster&rpar;는 오직 &#39;단일 AZ&#39;&lt;/span&gt;
    &lt;/div&gt;
    &lt;p class=&quot;dd-content&quot;&gt;
      클러스터는 최고의 네트워크 속도를 위해 물리적으로 가까이 뭉쳐야 하므로 &lt;span class=&quot;code-span&quot;&gt;여러 AZ에 걸쳐 생성할 수 없습니다.&lt;/span&gt;
      &lt;span class=&quot;sub-text&quot;&gt;👉 반면, &lt;strong&gt;분산&lpar;Spread&rpar;&lt;/strong&gt;과 &lt;strong&gt;파티션&lpar;Partition&rpar;&lt;/strong&gt; 그룹은 여러 AZ에 걸쳐서 배치 가능합니다.&lt;/span&gt;
    &lt;/p&gt;
  &lt;/div&gt;

  &lt;div class=&quot;dd-item&quot;&gt;
    &lt;div class=&quot;dd-header&quot;&gt;
      &lt;span class=&quot;dd-title&quot;&gt;2. 분산&lpar;Spread&rpar; vs 파티션&lpar;Partition&rpar; 구분법&lt;/span&gt;
      &lt;span class=&quot;dd-badge blue&quot;&gt;Tip&lt;/span&gt;
    &lt;/div&gt;
    &lt;p class=&quot;dd-content&quot;&gt;
      둘 다 하드웨어를 분리하지만, &lt;span class=&quot;code-span&quot;&gt;&#39;규모&#39;&lt;/span&gt;가 다릅니다.
      &lt;span class=&quot;sub-text&quot;&gt;
        • 분산: 인스턴스 단위 격리 &lpar;AZ당 7개 제한&rpar; → &lt;strong&gt;중요 DB&lt;/strong&gt;&lt;br /&gt;
        • 파티션: 그룹 단위 격리 &lpar;수백 개 가능&rpar; → &lt;strong&gt;Hadoop, Kafka&lt;/strong&gt;
      &lt;/span&gt;
    &lt;/p&gt;
  &lt;/div&gt;

  &lt;div class=&quot;dd-item&quot;&gt;
    &lt;div class=&quot;dd-header&quot;&gt;
      &lt;span class=&quot;dd-title&quot;&gt;3. 실행 중인 인스턴스는 이동 불가&lt;/span&gt;
    &lt;/div&gt;
    &lt;p class=&quot;dd-content&quot;&gt;
      이미 잘 돌아가고 있는 인스턴스를 나중에 배치 그룹으로 옮길 수는 없습니다.
      &lt;span class=&quot;sub-text&quot;&gt;👉 &lt;strong&gt;AMI&lpar;이미지&rpar;를 생성&lt;/strong&gt;한 뒤, 배치 그룹을 지정하여 &lt;strong&gt;새 인스턴스로 다시 시작&lpar;Launch&rpar;&lt;/strong&gt;해야 합니다.&lt;/span&gt;
    &lt;/p&gt;
  &lt;/div&gt;

&lt;/div&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;h3 id=&quot;보안그룹security-group&quot;&gt;보안그룹&lpar;Security Group&rpar;&lt;/h3&gt;

&lt;div class=&quot;story-box&quot;&gt;
  &lt;h4 style=&quot;color: #1e293b; font-weight: 800; margin-bottom: 1rem;&quot;&gt;EC2의 가상 방화벽, 보안 그룹&lpar;Security Group&rpar;&lt;/h4&gt;

  &lt;p&gt;보안 그룹은 EC2 인스턴스를 보호하기 위한 &lt;strong class=&quot;highlight-text&quot;&gt;가상 방화벽&lt;/strong&gt;입니다. 인스턴스로 들어오는 트래픽&lpar;Inbound&rpar;과 나가는 트래픽&lpar;Outbound&rpar;을 철저하게 검사하여 허용된 요청만 통과시킵니다.&lt;/p&gt;
&lt;/div&gt;

&lt;div class=&quot;info-box&quot;&gt;

&lt;div style=&quot;background-color: white; margin-top: 2rem; margin-bottom: 2rem; font-size: 0.9rem; letter-spacing: -0.03em; line-height: 1.5; max-width: 820px; margin-left: auto; margin-right: auto;&quot;&gt;

    &lt;div style=&quot;background-color: #f8fafc; border: 1px solid #cbd5e1; border-radius: 0.8rem; padding: 1.5rem; margin-bottom: 2rem; position: relative;&quot;&gt;

        &lt;h4 style=&quot;text-align: center; margin: 0 0 1.5rem 0; color: #334155; font-size: 1.1rem;&quot;&gt;
            🏰 &lt;strong&gt;이중 보안 시스템&lt;/strong&gt;으로 이해하기
        &lt;/h4&gt;

        &lt;div style=&quot;position: relative; padding: 2rem; background: #fff; border: 2px dashed #94a3b8; border-radius: 1rem; margin-bottom: 1rem;&quot;&gt;

            &lt;div style=&quot;position: absolute; top: -12px; left: 20px; background: #94a3b8; color: white; padding: 0.2rem 0.8rem; border-radius: 99px; font-size: 0.8rem; font-weight: 700;&quot;&gt;
                1차 관문: 네트워크 ACL &lpar;NACL&rpar;
            &lt;/div&gt;

            &lt;div style=&quot;position: absolute; top: 10px; right: 20px; color: #64748b; font-size: 0.75rem;&quot;&gt;
                🏢 &lt;strong&gt;아파트 정문 &lpar;서브넷 수준&rpar;&lt;/strong&gt;
            &lt;/div&gt;

            &lt;div style=&quot;border: 2px solid #3b82f6; background: #eff6ff; border-radius: 0.8rem; padding: 2rem 1.5rem 1.5rem 1.5rem; position: relative; margin-top: 1rem;&quot;&gt;

                &lt;div style=&quot;position: absolute; top: -12px; left: 20px; background: #3b82f6; color: white; padding: 0.2rem 0.8rem; border-radius: 99px; font-size: 0.8rem; font-weight: 700;&quot;&gt;
                    2차 관문: 보안 그룹 &lpar;SG&rpar;
                &lt;/div&gt;

                &lt;div style=&quot;position: absolute; top: 10px; right: 20px; color: #1e40af; font-size: 0.75rem;&quot;&gt;
                    🚪 &lt;strong&gt;우리집 현관문 &lpar;인스턴스 수준&rpar;&lt;/strong&gt;
                &lt;/div&gt;

                &lt;div style=&quot;background: white; border: 1px solid #bfdbfe; border-radius: 0.5rem; padding: 1rem; text-align: center; display: flex; align-items: center; justify-content: center; gap: 0.5rem;&quot;&gt;

                    &lt;i class=&quot;fas fa-server&quot; style=&quot;font-size: 1.5rem; color: #f97316;&quot;&gt;&lt;/i&gt;

                    &lt;div&gt;
                        &lt;strong style=&quot;color: #1e293b; display: block;&quot;&gt;EC2 인스턴스&lt;/strong&gt;
                        &lt;span style=&quot;font-size: 0.7rem; color: #64748b;&quot;&gt;&lpar;가장 소중한 자산&rpar;&lt;/span&gt;
                    &lt;/div&gt;

                &lt;/div&gt;

            &lt;/div&gt;

        &lt;/div&gt;

        &lt;p style=&quot;text-align: center; font-size: 0.85rem; color: #475569; margin: 0;&quot;&gt;
            트래픽은 &lt;strong&gt;NACL&lpar;서브넷&rpar;&lt;/strong&gt;을 먼저 통과한 뒤, &lt;strong&gt;보안 그룹&lpar;인스턴스&rpar;&lt;/strong&gt;을 통과해야 EC2에 도달합니다.
        &lt;/p&gt;

    &lt;/div&gt;
&lt;/div&gt;

&lt;div class=&quot;story-box&quot;&gt;
    &lt;p&gt;처음 보안 그룹을 생성하면 다음과 같은 &lt;strong&gt;초기 상태&lpar;Default&rpar;&lt;/strong&gt;를 가집니다.&lt;/p&gt;

    &lt;ul&gt;
      &lt;li&gt;&lt;strong style=&quot;color: #1e293b;&quot;&gt;인바운드&lpar;Inbound&rpar;:&lt;/strong&gt; &lt;span style=&quot;color: #ef4444; font-weight: 700;&quot;&gt;모두 차단 &lpar;Deny All&rpar;&lt;/span&gt; &lt;br /&gt; &lt;span style=&quot;color: #64748b;&quot;&gt;→ 규칙을 추가하지 않으면 아무도 들어올 수 없습니다. &lpar;암묵적 차단&rpar;&lt;/span&gt;&lt;/li&gt;
      &lt;li&gt;&lt;strong style=&quot;color: #1e293b;&quot;&gt;아웃바운드&lpar;Outbound&rpar;:&lt;/strong&gt; &lt;span style=&quot;color: #22c55e; font-weight: 700;&quot;&gt;모두 허용 &lpar;Allow All&rpar;&lt;/span&gt; &lt;br /&gt; &lt;span style=&quot;color: #64748b;&quot;&gt;→ 인스턴스에서 외부로 나가는 통신은 기본적으로 다 열려 있습니다.&lt;/span&gt;&lt;/li&gt;
    &lt;/ul&gt;
  &lt;/div&gt;

&lt;div class=&quot;info-box&quot;&gt;

&lt;div style=&quot;background-color: white; margin-top: 2rem; margin-bottom: 2rem; font-family: &#39;Apple SD Gothic Neo&#39;, sans-serif; font-size: 0.85rem; letter-spacing: -0.03em; line-height: 1.4; max-width: 820px; margin-left: auto; margin-right: auto;&quot;&gt;

            &lt;div style=&quot;display: grid; grid-template-columns: 1fr 1fr; gap: 1rem;&quot;&gt;

                &lt;div style=&quot;border: 2px solid #3b82f6; border-radius: 0.8rem; overflow: hidden; display: flex; flex-direction: column;&quot;&gt;
                    &lt;div style=&quot;background: #eff6ff; padding: 0.6rem; text-align: center; border-bottom: 1px solid #3b82f6;&quot;&gt;
                        &lt;div style=&quot;font-weight: 800; color: #1e40af; font-size: 1rem;&quot;&gt;보안 그룹 &lpar;SG&rpar;&lt;/div&gt;
                        &lt;div style=&quot;font-size: 0.75rem; color: #60a5fa;&quot;&gt;&quot;똑똑한 경호원 &lpar;Stateful&rpar;&quot;&lt;/div&gt;
                    &lt;/div&gt;

                    &lt;div style=&quot;padding: 0.8rem; flex: 1; display: flex; flex-direction: column; gap: 0.8rem;&quot;&gt;

                        &lt;div style=&quot;background: #fff; border: 1px solid #bfdbfe; border-radius: 0.5rem; padding: 0.5rem; text-align: center;&quot;&gt;
                            &lt;div style=&quot;font-size: 0.75rem; font-weight: 700; color: #1e40af; margin-bottom: 0.3rem;&quot;&gt;위치: 인스턴스 수준&lt;/div&gt;
                            &lt;div style=&quot;display: inline-block; position: relative;&quot;&gt;
                                &lt;i class=&quot;fas fa-server&quot; style=&quot;font-size: 2rem; color: #3b82f6;&quot;&gt;&lt;/i&gt;
                                &lt;i class=&quot;fas fa-shield-alt&quot; style=&quot;position: absolute; bottom: -5px; right: -5px; font-size: 1rem; color: #1e40af; background: white; border-radius: 50%;&quot;&gt;&lt;/i&gt;
                            &lt;/div&gt;
                            &lt;div style=&quot;font-size: 0.7rem; color: #64748b; margin-top: 0.2rem;&quot;&gt;개별 인스턴스 방어&lt;/div&gt;
                        &lt;/div&gt;

                        &lt;div style=&quot;background: #f0f9ff; border: 1px dashed #3b82f6; border-radius: 0.5rem; padding: 0.5rem; text-align: center;&quot;&gt;
                            &lt;strong style=&quot;color: #0369a1; display: block; font-size: 0.75rem; margin-bottom: 0.3rem;&quot;&gt;🧠 상태 저장 &lpar;Stateful&rpar;&lt;/strong&gt;
                            &lt;div style=&quot;display: flex; align-items: center; justify-content: center; gap: 0.3rem; font-size: 0.7rem; color: #475569;&quot;&gt;
                                &lt;span&gt;In&lt;/span&gt;
                                &lt;i class=&quot;fas fa-long-arrow-alt-right&quot; style=&quot;color: #3b82f6;&quot;&gt;&lt;/i&gt;
                                &lt;span style=&quot;background: white; border: 1px solid #cbd5e1; padding: 0.1rem 0.3rem; border-radius: 3px; font-weight: 700;&quot;&gt;기억&lt;/span&gt;
                                &lt;i class=&quot;fas fa-long-arrow-alt-right&quot; style=&quot;color: #3b82f6;&quot;&gt;&lt;/i&gt;
                                &lt;span&gt;Out&lpar;자동&rpar;&lt;/span&gt;
                            &lt;/div&gt;
                        &lt;/div&gt;

                        &lt;div style=&quot;background: #f8fafc; padding: 0.6rem; border-radius: 0.5rem; border: 1px solid #e2e8f0;&quot;&gt;
                            &lt;strong style=&quot;display: block; font-size: 0.75rem; color: #1e293b; margin-bottom: 0.5rem; text-align: center;&quot;&gt;📋 규칙 작동 원리&lt;/strong&gt;
                            &lt;div style=&quot;display: flex; flex-direction: column; gap: 0.5rem;&quot;&gt;

                                &lt;div style=&quot;display: flex; align-items: center; gap: 0.5rem; background: white; padding: 0.4rem; border-radius: 4px; border: 1px solid #cbd5e1;&quot;&gt;
                                    &lt;div style=&quot;background: #dcfce7; color: #166534; padding: 0.1rem 0.3rem; border-radius: 3px; font-weight: 700; font-size: 0.65rem; white-space: nowrap;&quot;&gt;허용&lpar;Allow&rpar;만&lt;/div&gt;
                                    &lt;i class=&quot;fas fa-random&quot; style=&quot;color: #94a3b8; font-size: 0.8rem;&quot;&gt;&lt;/i&gt;
                                    &lt;div style=&quot;font-size: 0.7rem; color: #475569;&quot;&gt;규칙 &lt;strong&gt;동시 평가&lt;/strong&gt; &lpar;순서 X&rpar;&lt;/div&gt;
                                &lt;/div&gt;

                                &lt;div style=&quot;display: flex; align-items: center; gap: 0.5rem; background: white; padding: 0.4rem; border-radius: 4px; border: 1px solid #cbd5e1;&quot;&gt;
                                    &lt;div style=&quot;display: flex; gap: 2px;&quot;&gt;
                                        &lt;span style=&quot;background: #e2e8f0; color: #475569; padding: 0.1rem 0.3rem; border-radius: 3px; font-size: 0.65rem; font-weight: 700;&quot;&gt;IP&lt;/span&gt;
                                        &lt;span style=&quot;background: #dbeafe; color: #1e40af; padding: 0.1rem 0.3rem; border-radius: 3px; font-size: 0.65rem; font-weight: 700;&quot;&gt;SG-ID&lt;/span&gt;
                                    &lt;/div&gt;
                                    &lt;i class=&quot;fas fa-arrow-right&quot; style=&quot;color: #94a3b8; font-size: 0.8rem;&quot;&gt;&lt;/i&gt;
                                    &lt;div style=&quot;font-size: 0.7rem; color: #475569;&quot;&gt;IP 및 &lt;strong&gt;다른 SG 참조&lt;/strong&gt; 가능&lt;/div&gt;
                                &lt;/div&gt;

                                &lt;div style=&quot;display: flex; align-items: center; gap: 0.5rem; background: white; padding: 0.4rem; border-radius: 4px; border: 1px solid #cbd5e1;&quot;&gt;
                                    &lt;i class=&quot;fas fa-edit&quot; style=&quot;color: #3b82f6; font-size: 0.8rem; width: 15px; text-align: center;&quot;&gt;&lt;/i&gt;
                                    &lt;div style=&quot;font-size: 0.7rem; color: #475569;&quot;&gt;
                                        &lt;strong&gt;시작 / 수정 시&lt;/strong&gt; 적용
                                    &lt;/div&gt;
                                &lt;/div&gt;

                            &lt;/div&gt;
                        &lt;/div&gt;

                    &lt;/div&gt;
                &lt;/div&gt;

                &lt;div style=&quot;border: 2px solid #94a3b8; border-radius: 0.8rem; overflow: hidden; display: flex; flex-direction: column;&quot;&gt;
                    &lt;div style=&quot;background: #f1f5f9; padding: 0.6rem; text-align: center; border-bottom: 1px solid #94a3b8;&quot;&gt;
                        &lt;div style=&quot;font-weight: 800; color: #475569; font-size: 1rem;&quot;&gt;네트워크 ACL &lpar;NACL&rpar;&lt;/div&gt;
                        &lt;div style=&quot;font-size: 0.75rem; color: #64748b;&quot;&gt;&quot;원칙적인 경비원 &lpar;Stateless&rpar;&quot;&lt;/div&gt;
                    &lt;/div&gt;

                    &lt;div style=&quot;padding: 0.8rem; flex: 1; display: flex; flex-direction: column; gap: 0.8rem;&quot;&gt;

                        &lt;div style=&quot;background: #fff; border: 1px solid #cbd5e1; border-radius: 0.5rem; padding: 0.5rem; text-align: center;&quot;&gt;
                            &lt;div style=&quot;font-size: 0.75rem; font-weight: 700; color: #475569; margin-bottom: 0.3rem;&quot;&gt;위치: 서브넷 수준&lt;/div&gt;
                            &lt;div style=&quot;display: inline-block; border: 2px dashed #94a3b8; padding: 0.3rem; border-radius: 0.4rem;&quot;&gt;
                                &lt;div style=&quot;display: grid; grid-template-columns: 1fr 1fr; gap: 2px;&quot;&gt;
                                    &lt;i class=&quot;fas fa-server&quot; style=&quot;font-size: 0.8rem; color: #cbd5e1;&quot;&gt;&lt;/i&gt;
                                    &lt;i class=&quot;fas fa-server&quot; style=&quot;font-size: 0.8rem; color: #cbd5e1;&quot;&gt;&lt;/i&gt;
                                    &lt;i class=&quot;fas fa-server&quot; style=&quot;font-size: 0.8rem; color: #cbd5e1;&quot;&gt;&lt;/i&gt;
                                    &lt;i class=&quot;fas fa-server&quot; style=&quot;font-size: 0.8rem; color: #cbd5e1;&quot;&gt;&lt;/i&gt;
                                &lt;/div&gt;
                            &lt;/div&gt;
                            &lt;div style=&quot;font-size: 0.7rem; color: #64748b; margin-top: 0.2rem;&quot;&gt;서브넷 전체 방어&lt;/div&gt;
                        &lt;/div&gt;

                        &lt;div style=&quot;background: #f8fafc; border: 1px dashed #94a3b8; border-radius: 0.5rem; padding: 0.5rem; text-align: center;&quot;&gt;
                            &lt;strong style=&quot;color: #475569; display: block; font-size: 0.75rem; margin-bottom: 0.3rem;&quot;&gt;🤖 비상태 &lpar;Stateless&rpar;&lt;/strong&gt;
                            &lt;div style=&quot;display: flex; align-items: center; justify-content: center; gap: 0.3rem; font-size: 0.7rem; color: #475569;&quot;&gt;
                                &lt;span&gt;In&lt;/span&gt;
                                &lt;i class=&quot;fas fa-long-arrow-alt-right&quot; style=&quot;color: #94a3b8;&quot;&gt;&lt;/i&gt;
                                &lt;span style=&quot;background: white; border: 1px solid #cbd5e1; padding: 0.1rem 0.3rem; border-radius: 3px; font-weight: 700;&quot;&gt;망각&lt;/span&gt;
                                &lt;i class=&quot;fas fa-long-arrow-alt-right&quot; style=&quot;color: #94a3b8;&quot;&gt;&lt;/i&gt;
                                &lt;span&gt;Out&lpar;재검사&rpar;&lt;/span&gt;
                            &lt;/div&gt;
                        &lt;/div&gt;

                        &lt;div style=&quot;background: #f8fafc; padding: 0.6rem; border-radius: 0.5rem; border: 1px solid #e2e8f0;&quot;&gt;
                            &lt;strong style=&quot;display: block; font-size: 0.75rem; color: #1e293b; margin-bottom: 0.5rem; text-align: center;&quot;&gt;📋 규칙 작동 원리&lt;/strong&gt;
                            &lt;div style=&quot;display: flex; flex-direction: column; gap: 0.5rem;&quot;&gt;

                                &lt;div style=&quot;display: flex; align-items: center; gap: 0.5rem; background: white; padding: 0.4rem; border-radius: 4px; border: 1px solid #cbd5e1;&quot;&gt;
                                    &lt;div style=&quot;display: flex; flex-direction: column; gap: 2px;&quot;&gt;
                                        &lt;span style=&quot;background: #dcfce7; color: #166534; padding: 0.1rem 0.3rem; border-radius: 3px; font-weight: 700; font-size: 0.65rem; white-space: nowrap;&quot;&gt;허용&lpar;Allow&rpar;&lt;/span&gt;
                                        &lt;span style=&quot;background: #fee2e2; color: #991b1b; padding: 0.1rem 0.3rem; border-radius: 3px; font-weight: 700; font-size: 0.65rem; white-space: nowrap;&quot;&gt;거부&lpar;Deny&rpar;&lt;/span&gt;
                                    &lt;/div&gt;
                                    &lt;i class=&quot;fas fa-sort-numeric-down&quot; style=&quot;color: #94a3b8; font-size: 0.8rem;&quot;&gt;&lt;/i&gt;
                                    &lt;div style=&quot;font-size: 0.7rem; color: #475569;&quot;&gt;번호 &lt;strong&gt;순서대로&lt;/strong&gt; 평가 &lpar;직렬&rpar;&lt;/div&gt;
                                &lt;/div&gt;

                                &lt;div style=&quot;display: flex; align-items: center; gap: 0.5rem; background: white; padding: 0.4rem; border-radius: 4px; border: 1px solid #cbd5e1;&quot;&gt;
                                    &lt;div style=&quot;display: flex; gap: 2px;&quot;&gt;
                                        &lt;span style=&quot;background: #e2e8f0; color: #475569; padding: 0.1rem 0.3rem; border-radius: 3px; font-size: 0.65rem; font-weight: 700;&quot;&gt;IP Only&lt;/span&gt;
                                    &lt;/div&gt;
                                    &lt;i class=&quot;fas fa-arrow-right&quot; style=&quot;color: #94a3b8; font-size: 0.8rem;&quot;&gt;&lt;/i&gt;
                                    &lt;div style=&quot;font-size: 0.7rem; color: #475569;&quot;&gt;특정 &lt;strong&gt;IP 주소만&lt;/strong&gt; 참조 가능&lt;/div&gt;
                                &lt;/div&gt;

                                &lt;div style=&quot;display: flex; align-items: center; gap: 0.5rem; background: white; padding: 0.4rem; border-radius: 4px; border: 1px solid #cbd5e1;&quot;&gt;
                                    &lt;i class=&quot;fas fa-bolt&quot; style=&quot;color: #eab308; font-size: 0.8rem; width: 15px; text-align: center;&quot;&gt;&lt;/i&gt;
                                    &lt;div style=&quot;font-size: 0.7rem; color: #475569;&quot;&gt;
                                        &lt;strong&gt;즉시 적용&lt;/strong&gt;
                                    &lt;/div&gt;
                                &lt;/div&gt;

                            &lt;/div&gt;
                        &lt;/div&gt;

                    &lt;/div&gt;
                &lt;/div&gt;
            &lt;/div&gt;

        &lt;/div&gt;
    &lt;/div&gt;
&lt;/div&gt;

&lt;div class=&quot;info-box&quot;&gt;
  
  &lt;div style=&quot;margin-bottom: 1.5rem;&quot;&gt;
    &lt;h4 style=&quot;margin: 0; color: #1e293b; font-weight: 800;&quot;&gt;✔️ 보안 그룹 vs NACL 실전 포인트 &lpar;Deep Dive&rpar;&lt;/h4&gt;
  &lt;/div&gt;

  &lt;div class=&quot;deep-dive-list&quot;&gt;

    &lt;div class=&quot;dd-item&quot;&gt;
      &lt;div class=&quot;dd-header&quot;&gt;
        &lt;span class=&quot;dd-title&quot;&gt;1. &quot;상태 저장&lpar;Stateful&rpar;&quot;의 진짜 의미&lt;/span&gt;
        &lt;span class=&quot;dd-badge blue&quot;&gt;핵심&lt;/span&gt;
      &lt;/div&gt;
      &lt;p class=&quot;dd-content&quot;&gt;
        보안 그룹은 들어오는 요청&lpar;Inbound&rpar;을 허용하면, 그 응답으로 나가는 트래픽&lpar;Outbound&rpar;은 &lt;span class=&quot;code-span&quot;&gt;규칙과 상관없이 자동으로 허용&lt;/span&gt;됩니다. &lpar;왕복 티켓&rpar;
        &lt;span class=&quot;sub-text&quot;&gt;👉 반면 &lt;strong&gt;NACL은 Stateless&lt;/strong&gt;이므로, 들어올 때 허용했어도 나가는 규칙&lpar;Outbound&rpar;이 없으면 응답이 차단됩니다.&lt;/span&gt;
      &lt;/p&gt;
    &lt;/div&gt;

    &lt;div class=&quot;dd-item&quot;&gt;
      &lt;div class=&quot;dd-header&quot;&gt;
          &lt;span class=&quot;dd-title&quot;&gt;2. 해커 IP를 차단하려면? 오직 NACL&lt;/span&gt;
      &lt;/div&gt;
      &lt;p class=&quot;dd-content&quot;&gt;
          보안 그룹은 &lt;strong&gt;&#39;허용&lpar;Allow&rpar;&#39; 규칙만&lt;/strong&gt; 존재하며, 규칙에 없는 트래픽은 &lt;span class=&quot;code-span&quot;&gt;암묵적으로 모두 차단&lt;/span&gt;됩니다. &quot;특정 IP만 막겠다&lpar;Deny&rpar;&quot;는 설정은 불가능합니다.
          
          &lt;span class=&quot;sub-text gray-box&quot;&gt;
              • 특정 공격자 IP 차단&lpar;Deny&rpar; → &lt;strong&gt;NACL 사용&lt;/strong&gt;&lt;br /&gt;
              • 서비스 포트 개방&lpar;Allow&rpar; → &lt;strong&gt;보안 그룹 사용&lt;/strong&gt;
          &lt;/span&gt;
      &lt;/p&gt;
    &lt;/div&gt;

    &lt;div class=&quot;dd-item&quot;&gt;
      &lt;div class=&quot;dd-header&quot;&gt;
        &lt;span class=&quot;dd-title&quot;&gt;3. 보안 그룹은 &#39;신분증&#39;, NACL은 &#39;지명수배&#39;&lt;/span&gt;
        &lt;span class=&quot;dd-badge pink&quot;&gt;비유&lt;/span&gt;
      &lt;/div&gt;
      &lt;p class=&quot;dd-content&quot;&gt;
        보안 그룹은 &lt;span class=&quot;code-span&quot;&gt;다른 보안 그룹 ID를 참조&lt;/span&gt;할 수 있습니다. &quot;웹 서버 그룹&lpar;A&rpar;에서 오는 트래픽만 DB 그룹&lpar;B&rpar;이 허용한다&quot;는 식의 유연한 설정이 가능합니다.
        &lt;span class=&quot;sub-text&quot;&gt;👉 반면 NACL은 오직 &lt;strong&gt;IP 대역&lpar;CIDR&rpar;&lt;/strong&gt;으로만 규칙을 설정할 수 있습니다.&lt;/span&gt;
      &lt;/p&gt;
    &lt;/div&gt;

  &lt;/div&gt;
&lt;/div&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;h3 id=&quot;user-data&quot;&gt;User Data&lt;/h3&gt;

&lt;div class=&quot;info-box&quot;&gt;
&lt;div style=&quot;background-color: white; margin-top: 2rem; margin-bottom: 2rem; font-family: &#39;Apple SD Gothic Neo&#39;, sans-serif; font-size: 0.85rem; letter-spacing: -0.03em; line-height: 1.4; max-width: 800px; margin-left: auto; margin-right: auto; color: #334155;&quot;&gt;

  &lt;div style=&quot;display: flex; gap: 0.5rem; align-items: stretch; margin-bottom: 2rem;&quot;&gt;

    &lt;div style=&quot;flex: 1; border: 1px solid #e2e8f0; border-radius: 0.8rem; overflow: hidden; display: flex; flex-direction: column; min-width: 0;&quot;&gt;
      &lt;div style=&quot;background: #f1f5f9; padding: 0.6rem; text-align: center; border-bottom: 1px solid #e2e8f0;&quot;&gt;
        &lt;div style=&quot;font-weight: 800; color: #475569; font-size: 0.9rem;&quot;&gt;1. 인스턴스 시작&lt;/div&gt;
        &lt;div style=&quot;font-size: 0.7rem; color: #94a3b8;&quot;&gt;&lpar;Trigger&rpar;&lt;/div&gt;
      &lt;/div&gt;
      &lt;div style=&quot;padding: 1rem; flex: 1; display: flex; flex-direction: column; align-items: center; justify-content: center; background: white;&quot;&gt;
        &lt;div style=&quot;background: #f8fafc; border: 1px solid #cbd5e1; width: 50px; height: 50px; border-radius: 50%; display: flex; align-items: center; justify-content: center; margin-bottom: 0.5rem;&quot;&gt;
          &lt;i class=&quot;fas fa-power-off&quot; style=&quot;font-size: 1.5rem; color: #475569;&quot;&gt;&lt;/i&gt;
        &lt;/div&gt;
        &lt;div style=&quot;text-align: center; font-size: 0.8rem; color: #334155; font-weight: 700;&quot;&gt;
          서버 전원 ON
        &lt;/div&gt;
      &lt;/div&gt;
    &lt;/div&gt;

    &lt;div style=&quot;display: flex; align-items: center; justify-content: center; color: #cbd5e1;&quot;&gt;
      &lt;i class=&quot;fas fa-chevron-right&quot; style=&quot;font-size: 1.2rem;&quot;&gt;&lt;/i&gt;
    &lt;/div&gt;

    &lt;div style=&quot;flex: 1.2; border: 1px solid #e2e8f0; border-radius: 0.8rem; overflow: hidden; display: flex; flex-direction: column; min-width: 0;&quot;&gt;
      &lt;div style=&quot;background: #f1f5f9; padding: 0.6rem; text-align: center; border-bottom: 1px solid #e2e8f0;&quot;&gt;
        &lt;div style=&quot;font-weight: 800; color: #475569; font-size: 0.9rem;&quot;&gt;2. User Data 실행&lt;/div&gt;
        &lt;div style=&quot;font-size: 0.7rem; color: #94a3b8;&quot;&gt;&lpar;Script&rpar;&lt;/div&gt;
      &lt;/div&gt;
      &lt;div style=&quot;padding: 0.8rem; flex: 1; display: flex; flex-direction: column; background: white; justify-content: center;&quot;&gt;
        &lt;div style=&quot;background: #1e293b; border-radius: 0.4rem; padding: 0.6rem; color: #e2e8f0; font-family: monospace; font-size: 0.7rem; margin-bottom: 0.5rem; position: relative; border: 1px solid #334155;&quot;&gt;
          &lt;div style=&quot;color: #60a5fa; margin-bottom: 4px;&quot;&gt;&amp;gt;_ #!/bin/bash&lt;/div&gt;
          &lt;div&gt;apt-get update -y&lt;/div&gt;
          &lt;div&gt;yum install -y httpd&lt;/div&gt;
          &lt;div style=&quot;color: #94a3b8;&quot;&gt;...running...&lt;/div&gt;
        &lt;/div&gt;
        &lt;div style=&quot;display: flex; justify-content: center; gap: 0.3rem;&quot;&gt;
          &lt;span style=&quot;background: #f1f5f9; color: #475569; padding: 0.1rem 0.4rem; border-radius: 3px; font-size: 0.7rem; font-weight: 700; border: 1px solid #e2e8f0;&quot;&gt;Root 권한&lt;/span&gt;
          &lt;span style=&quot;background: #f1f5f9; color: #475569; padding: 0.1rem 0.4rem; border-radius: 3px; font-size: 0.7rem; font-weight: 700; border: 1px solid #e2e8f0;&quot;&gt;단 1회&lt;/span&gt;
        &lt;/div&gt;
      &lt;/div&gt;
    &lt;/div&gt;

    &lt;div style=&quot;display: flex; align-items: center; justify-content: center; color: #cbd5e1;&quot;&gt;
      &lt;i class=&quot;fas fa-chevron-right&quot; style=&quot;font-size: 1.2rem;&quot;&gt;&lt;/i&gt;
    &lt;/div&gt;

    &lt;div style=&quot;flex: 1.2; border: 1px solid #e2e8f0; border-radius: 0.8rem; overflow: hidden; display: flex; flex-direction: column; min-width: 0;&quot;&gt;
      &lt;div style=&quot;background: #f1f5f9; padding: 0.6rem; text-align: center; border-bottom: 1px solid #e2e8f0;&quot;&gt;
        &lt;div style=&quot;font-weight: 800; color: #475569; font-size: 0.9rem;&quot;&gt;3. 부트스트랩 완료&lt;/div&gt;
        &lt;div style=&quot;font-size: 0.7rem; color: #94a3b8;&quot;&gt;&lpar;Result&rpar;&lt;/div&gt;
      &lt;/div&gt;
      &lt;div style=&quot;padding: 0.8rem; flex: 1; display: flex; align-items: center; gap: 0.8rem; background: white;&quot;&gt;
        &lt;div style=&quot;position: relative; flex-shrink: 0;&quot;&gt;
           &lt;div style=&quot;background: #f0fdfa; border: 1px solid #ccfbf1; border-radius: 0.5rem; width: 46px; height: 46px; display: grid; grid-template-columns: 1fr 1fr; align-items: center; justify-items: center; padding: 2px;&quot;&gt;
             &lt;i class=&quot;fas fa-couch&quot; style=&quot;color: #0d9488; font-size: 0.7rem;&quot;&gt;&lt;/i&gt;
             &lt;i class=&quot;fas fa-tv&quot; style=&quot;color: #0d9488; font-size: 0.7rem;&quot;&gt;&lt;/i&gt;
             &lt;i class=&quot;fas fa-bed&quot; style=&quot;color: #0d9488; font-size: 0.7rem;&quot;&gt;&lt;/i&gt;
             &lt;i class=&quot;fas fa-wifi&quot; style=&quot;color: #0d9488; font-size: 0.7rem;&quot;&gt;&lt;/i&gt;
           &lt;/div&gt;
           &lt;i class=&quot;fas fa-check-circle&quot; style=&quot;position: absolute; bottom: -4px; right: -4px; color: #0d9488; background: white; border-radius: 50%; font-size: 0.9rem;&quot;&gt;&lt;/i&gt;
        &lt;/div&gt;
        &lt;div style=&quot;display: flex; flex-direction: column; gap: 0.2rem;&quot;&gt;
          &lt;div style=&quot;font-size: 0.75rem; color: #334155;&quot;&gt;&lt;strong&gt;풀옵션 입주&lt;/strong&gt; 완료&lt;/div&gt;
          &lt;div style=&quot;height: 1px; background: #e2e8f0; width: 100%; margin: 2px 0;&quot;&gt;&lt;/div&gt;
          &lt;div style=&quot;font-size: 0.7rem; color: #64748b;&quot;&gt;업데이트 OK&lt;/div&gt;
          &lt;div style=&quot;font-size: 0.7rem; color: #64748b;&quot;&gt;설정 OK&lt;/div&gt;
        &lt;/div&gt;
      &lt;/div&gt;
    &lt;/div&gt;

  &lt;/div&gt;

  &lt;div style=&quot;background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 0.8rem; padding: 1.2rem; text-align: center;&quot;&gt;
    
    &lt;div style=&quot;display: inline-block; background: white; border: 1px dashed #94a3b8; padding: 0.8rem; border-radius: 0.5rem;&quot;&gt;
      &lt;span style=&quot;color: #475569; font-size: 0.9rem;&quot;&gt;
        &quot;EC2에서 &lt;strong style=&quot;color: #3b82f6;&quot;&gt;Bootstrap&lpar;행위&rpar;&lt;/strong&gt;을 하기 위해&lt;br /&gt;
        사용하는 기능이 바로 &lt;strong style=&quot;color: #f59e0b;&quot;&gt;User Data&lpar;도구&rpar;&lt;/strong&gt;이다.&quot;
      &lt;/span&gt;
    &lt;/div&gt;

    &lt;div style=&quot;margin-top: 1rem; display: flex; justify-content: center; gap: 0.5rem; font-size: 0.8rem; color: #64748b;&quot;&gt;
      &lt;div style=&quot;display: flex; align-items: center; gap: 5px;&quot;&gt;
        &lt;i class=&quot;fas fa-check-circle&quot; style=&quot;color: #10b981;&quot;&gt;&lt;/i&gt; AWS: &lt;strong&gt;User Data&lt;/strong&gt;
      &lt;/div&gt;
      &lt;div style=&quot;width: 1px; background: #cbd5e1;&quot;&gt;&lt;/div&gt;
      &lt;div style=&quot;display: flex; align-items: center; gap: 5px;&quot;&gt;
        &lt;i class=&quot;fas fa-check-circle&quot; style=&quot;color: #10b981;&quot;&gt;&lt;/i&gt; Azure: &lt;strong&gt;Custom Data&lt;/strong&gt;
      &lt;/div&gt;
      &lt;div style=&quot;width: 1px; background: #cbd5e1;&quot;&gt;&lt;/div&gt;
      &lt;div style=&quot;display: flex; align-items: center; gap: 5px;&quot;&gt;
        &lt;i class=&quot;fas fa-check-circle&quot; style=&quot;color: #10b981;&quot;&gt;&lt;/i&gt; GCP: &lt;strong&gt;Startup Script&lt;/strong&gt;
      &lt;/div&gt;
    &lt;/div&gt;
    &lt;div style=&quot;margin-top: 0.5rem; font-size: 0.75rem; color: #94a3b8;&quot;&gt;
      &lpar;클라우드마다 이름은 다르지만, 부트스트랩 기능은 모두 동일합니다&rpar;
    &lt;/div&gt;

  &lt;/div&gt;

&lt;/div&gt;
&lt;/div&gt;

&lt;div class=&quot;story-box&quot;&gt;
  &lt;p&gt;📦 &lt;strong class=&quot;highlight-text&quot;&gt;User Data &lpar;사용자 데이터&rpar;&lt;/strong&gt; : EC2 서버가 켜지자마자 실행되는 할 일 목록 &lpar;Shell Script&rpar;&lt;br /&gt;
🚀 &lt;strong class=&quot;highlight-text&quot;&gt;OS의 부트스트랩&lt;/strong&gt; : 서버 시작 시 특정 명령을 자동으로 실행하는 행위&lt;/p&gt;
&lt;/div&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;h3 id=&quot;탄력적-ipelastic-ip--eip&quot;&gt;탄력적 IP&lpar;Elastic IP / EIP&rpar;&lt;/h3&gt;

&lt;div class=&quot;story-box&quot;&gt;
  &lt;p&gt;EC2를 생성할 때 할당받는 일반 공인 IP는 인스턴스를 &lt;strong class=&quot;highlight-text&quot;&gt;중지&lpar;Stop&rpar;하고 다시 시작&lpar;Start&rpar;하면 IP 주소가 변경&lt;/strong&gt;됩니다. 서버의 주소가 계속 바뀐다면 사용자가 접속할 수 없겠죠? 이를 해결하기 위해 고정된 IP 주소인 &lt;strong&gt;탄력적 IP&lpar;Elastic IP&rpar;&lt;/strong&gt;를 사용합니다.&lt;/p&gt;
&lt;/div&gt;

&lt;div class=&quot;info-box&quot;&gt;
&lt;div style=&quot;margin-top: 2rem; margin-bottom: 2rem; font-family: &#39;Apple SD Gothic Neo&#39;, sans-serif; font-size: 0.9rem; letter-spacing: -0.03em; line-height: 1.4; max-width: 820px; margin-left: auto; margin-right: auto;&quot;&gt;

  &lt;div style=&quot;display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; margin-bottom: 1rem;&quot;&gt;
    
    &lt;div style=&quot;border: 1px dashed #94a3b8; border-radius: 0.6rem; padding: 1rem; background: #f8fafc; display: flex; flex-direction: column; align-items: center; justify-content: center; text-align: center;&quot;&gt;
      &lt;strong style=&quot;color: #64748b; font-size: 0.9rem; margin-bottom: 0.5rem;&quot;&gt;일반 Public IP&lt;/strong&gt;
      
      &lt;div style=&quot;display: flex; align-items: center; gap: 0.5rem; margin-bottom: 0.5rem;&quot;&gt;
        &lt;div style=&quot;position: relative;&quot;&gt;
          &lt;i class=&quot;fas fa-server&quot; style=&quot;font-size: 2rem; color: #cbd5e1;&quot;&gt;&lt;/i&gt;
          &lt;i class=&quot;fas fa-sync-alt&quot; style=&quot;position: absolute; top: 50%; left: 50%; transform: translate&lpar;-50%, -50%&rpar;; color: #ef4444; font-size: 1rem; background: rgba&lpar;255,255,255,0.8&rpar;; border-radius: 50%;&quot;&gt;&lt;/i&gt;
        &lt;/div&gt;
        &lt;i class=&quot;fas fa-arrow-right&quot; style=&quot;color: #94a3b8;&quot;&gt;&lt;/i&gt;
        &lt;div style=&quot;display: flex; flex-direction: column; font-family: monospace; font-size: 0.8rem;&quot;&gt;
          &lt;span style=&quot;color: #94a3b8; text-decoration: line-through;&quot;&gt;1.2.3.4&lt;/span&gt;
          &lt;span style=&quot;color: #ef4444; font-weight: 700;&quot;&gt;5.6.7.8 &lpar;New&rpar;&lt;/span&gt;
        &lt;/div&gt;
      &lt;/div&gt;
      
      &lt;div style=&quot;font-size: 0.8rem; color: #475569; background: white; padding: 0.3rem 0.6rem; border-radius: 4px; border: 1px solid #e2e8f0;&quot;&gt;
        EC2 인스턴스를 중지 후 재시작&lt;br /&gt;→ &lt;strong&gt;Public IP가 변경&lt;/strong&gt;
      &lt;/div&gt;
    &lt;/div&gt;

    &lt;div style=&quot;border: 2px solid #3b82f6; border-radius: 0.6rem; padding: 1rem; background: #eff6ff; display: flex; flex-direction: column; align-items: center; justify-content: center; text-align: center;&quot;&gt;
      &lt;strong style=&quot;color: #1e40af; font-size: 0.9rem; margin-bottom: 0.5rem;&quot;&gt;탄력적 IP &lpar;EIP&rpar;&lt;/strong&gt;

      &lt;div style=&quot;display: flex; align-items: center; gap: 0.5rem; margin-bottom: 0.5rem;&quot;&gt;
        &lt;i class=&quot;fas fa-server&quot; style=&quot;font-size: 2rem; color: #3b82f6;&quot;&gt;&lt;/i&gt;
        &lt;div style=&quot;height: 2px; width: 20px; background: #3b82f6;&quot;&gt;&lt;/div&gt;
        &lt;div style=&quot;background: #1e3a8a; color: white; padding: 0.3rem 0.6rem; border-radius: 4px; font-family: monospace; font-size: 0.85rem; font-weight: 700; display: flex; align-items: center; gap: 5px;&quot;&gt;
          &lt;i class=&quot;fas fa-map-pin&quot; style=&quot;color: #fbbf24;&quot;&gt;&lt;/i&gt; 54.123.x.x
        &lt;/div&gt;
      &lt;/div&gt;

      &lt;div style=&quot;font-size: 0.8rem; color: #1e3a8a;&quot;&gt;
        인스턴스에 &lt;strong&gt;고정된 공용 IP&lt;/strong&gt;가 필요할 경우
      &lt;/div&gt;
    &lt;/div&gt;

  &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;

&lt;div class=&quot;story-box&quot; style=&quot;margin-bottom: 0rem;&quot;&gt;
  &lt;p&gt;EIP는 단순히 ‘고정 IP’를 제공하는 것 이상의 의미가 있습니다. 인스턴스에 장애가 발생했을 때, EIP 주소의 연결을 &lt;strong class=&quot;highlight-text&quot;&gt;건강한 인스턴스로 즉시 재연결&lpar;Remapping&rpar;&lt;/strong&gt;하여 서비스 중단을 마스킹할 수 있습니다.&lt;/p&gt;

  &lt;p&gt;하지만 IPv4 주소는 전 세계적으로 부족한 자원입니다. AWS는 사용자가 IP를 낭비하지 않도록 독특한 과금 정책을 가지고 있습니다.&lt;/p&gt;
&lt;/div&gt;
&lt;div class=&quot;info-box&quot; style=&quot;margin-bottom:2.5rem&quot;&gt;
  &lt;div style=&quot;display: grid; grid-template-columns: 1fr 2fr; gap: 1rem;&quot;&gt;
    &lt;div style=&quot;background: white; border: 1px solid #e2e8f0; border-radius: 0.6rem; padding: 0.8rem; display: flex; align-items: center; justify-content: center; gap: 0.5rem;&quot;&gt;
      &lt;div style=&quot;text-align: center;&quot;&gt;
        &lt;i class=&quot;fas fa-server&quot; style=&quot;color: #64748b;&quot;&gt;&lt;/i&gt;
        &lt;div style=&quot;font-size: 0.75rem; color: #64748b;&quot;&gt;1 인스턴스&lt;/div&gt;
      &lt;/div&gt;
      &lt;i class=&quot;fas fa-long-arrow-alt-right&quot; style=&quot;color: #3b82f6;&quot;&gt;&lt;/i&gt;
      &lt;div style=&quot;text-align: center;&quot;&gt;
        &lt;i class=&quot;fas fa-tag&quot; style=&quot;color: #3b82f6;&quot;&gt;&lt;/i&gt;
        &lt;div style=&quot;font-size: 0.75rem; color: #1e40af; font-weight: 700;&quot;&gt;1 EIP&lt;/div&gt;
      &lt;/div&gt;
    &lt;/div&gt;
    &lt;div style=&quot;background: #fff7ed; border: 1px solid #fed7aa; border-radius: 0.6rem; padding: 0.8rem; display: flex; align-items: center; gap: 1rem;&quot;&gt;
      &lt;div style=&quot;background: #fff; width: 40px; height: 40px; border-radius: 50%; display: flex; align-items: center; justify-content: center; border: 2px solid #f97316; flex-shrink: 0;&quot;&gt;
        &lt;i class=&quot;fas fa-dollar-sign&quot; style=&quot;color: #f97316; font-size: 1.2rem;&quot;&gt;&lt;/i&gt;
      &lt;/div&gt;
      &lt;div style=&quot;font-size: 0.8rem; color: #9a3412; line-height: 1.3;&quot;&gt;
        &lt;strong&gt;⚠️ 비용 주의:&lt;/strong&gt; 릴리즈&lpar;반납&rpar; 하지 않으면 소유&lt;br /&gt;
        → 연결 안 된&lpar;미연결&rpar; EIP도 &lt;strong&gt;비용 발생&lt;/strong&gt;
      &lt;/div&gt;
    &lt;/div&gt;
  &lt;/div&gt;
&lt;/div&gt;

&lt;div style=&quot;margin-bottom: 1.5rem;&quot;&gt;
  &lt;h4 style=&quot;margin: 0; color: #1e293b; font-weight: 800;&quot;&gt;✔️ EIP 아키텍처 패턴 &lpar;Deep Dive&rpar;&lt;/h4&gt;
&lt;/div&gt;

&lt;div class=&quot;deep-dive-list&quot;&gt;

  &lt;div class=&quot;dd-item&quot;&gt;
    &lt;div class=&quot;dd-header&quot;&gt;
      &lt;span class=&quot;dd-title&quot;&gt;1. 장애 조치용으로 사용 &lpar;Masking Failure&rpar;&lt;/span&gt;
    &lt;/div&gt;
    &lt;p class=&quot;dd-content&quot;&gt;
      소프트웨어적인 문제로 인스턴스가 먹통이 되었을 때, 엔지니어가 EIP의 연결 대상을 &lt;span class=&quot;code-span&quot;&gt;대기 중인&lpar;Standby&rpar; 인스턴스로 즉시 변경&lt;/span&gt;하여 서비스 다운타임을 최소화할 수 있습니다.
    &lt;/p&gt;
  &lt;/div&gt;

  &lt;div class=&quot;dd-item&quot;&gt;
    &lt;div class=&quot;dd-header&quot;&gt;
      &lt;span class=&quot;dd-title&quot;&gt;2. 되도록 EIP 대신 ELB를 쓰세요&lt;/span&gt;
      &lt;span class=&quot;dd-badge green&quot;&gt;권장&lt;/span&gt;
    &lt;/div&gt;
    &lt;p class=&quot;dd-content&quot;&gt;
      EIP는 리전당 &lt;strong&gt;기본 5개로 제한&lt;/strong&gt;&lpar;Soft Limit&rpar;되어 있습니다. 확장성 있는 서비스를 위해서는 고정 IP&lpar;EIP&rpar;에 의존하기보다, &lt;span class=&quot;code-span&quot;&gt;로드 밸런서&lpar;ELB&rpar;의 DNS 주소&lt;/span&gt;를 사용하는 것이 훨씬 좋은 아키텍처입니다.
    &lt;/p&gt;
  &lt;/div&gt;

&lt;/div&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;h3 id=&quot;amiamazon-machine-image&quot;&gt;AMI&lpar;Amazon Machine Image&rpar;&lt;/h3&gt;

&lt;div class=&quot;story-box&quot;&gt;
  &lt;p&gt;컴퓨터를 새로 살 때마다 윈도우를 설치하고, 한글/오피스를 깔고, 환경 설정을 다시 하는 것은 매우 번거롭습니다. 만약 내 컴퓨터의 현재 상태를 &lt;strong&gt;그대로 복제해서 ‘틀&lpar;Mold&rpar;’로 만들어둔다면&lt;/strong&gt; 어떨까요?&lt;/p&gt;

  &lt;p&gt;&lt;strong&gt;AMI&lpar;Amazon Machine Image&rpar;&lt;/strong&gt;가 바로 그 역할을 합니다. EC2 인스턴스를 실행하기 위해 필요한 운영체제, 애플리케이션, 설정값 등을 모두 담고 있는 &lt;strong&gt;‘마스터 이미지’&lt;/strong&gt;입니다.&lt;/p&gt;
&lt;/div&gt;

&lt;div class=&quot;info-box&quot;&gt;
&lt;div style=&quot;background-color: white; margin-bottom: 2rem; font-family: &#39;Apple SD Gothic Neo&#39;, sans-serif; font-size: 0.85rem; letter-spacing: -0.03em; line-height: 1.4; max-width: 820px; margin-left: auto; margin-right: auto; color: #334155;&quot;&gt;
  &lt;div style=&quot;display: flex; gap: 1rem; border: 2px solid #cbd5e1; border-radius: 0.8rem; padding: 1.5rem 1rem; margin-bottom: 1rem; align-items: center; background: #f8fafc;&quot;&gt;  
    &lt;div style=&quot;text-align: center; min-width: 100px;&quot;&gt;
      &lt;i class=&quot;fas fa-save&quot; style=&quot;font-size: 2.5rem; color: #475569; margin-bottom: 0.5rem;&quot;&gt;&lt;/i&gt;
      &lt;div style=&quot;font-weight: 800; font-size: 0.9rem; color: #1e293b;&quot;&gt;AMI&lt;/div&gt;
      &lt;div style=&quot;font-size: 0.7rem; color: #64748b;&quot;&gt;&lpar;붕어빵 틀&rpar;&lt;/div&gt;
    &lt;/div&gt;
    &lt;div style=&quot;flex: 1; border-left: 2px dashed #cbd5e1; padding-left: 1rem;&quot;&gt;
      &lt;div style=&quot;font-weight: 800; color: #334155; font-size: 0.95rem; margin-bottom: 0.5rem;&quot;&gt;
        EC2 인스턴스를 찍어내는 &lt;span style=&quot;color: #2563eb;&quot;&gt;완벽한 설계도&lt;/span&gt;
      &lt;/div&gt;
      &lt;div style=&quot;display: flex; gap: 0.3rem; margin-bottom: 0.8rem; flex-wrap: wrap;&quot;&gt;
        &lt;span style=&quot;background: white; border: 1px solid #94a3b8; padding: 0.2rem 0.5rem; border-radius: 4px; font-size: 0.75rem; color: #475569;&quot;&gt;운영 체제&lt;/span&gt;
        &lt;span style=&quot;background: white; border: 1px solid #94a3b8; padding: 0.2rem 0.5rem; border-radius: 4px; font-size: 0.75rem; color: #475569;&quot;&gt;설치된 프로그램&lt;/span&gt;
        &lt;span style=&quot;background: white; border: 1px solid #94a3b8; padding: 0.2rem 0.5rem; border-radius: 4px; font-size: 0.75rem; color: #475569;&quot;&gt;권한/설정&lt;/span&gt;
      &lt;/div&gt;
      &lt;div style=&quot;font-size: 0.8rem; color: #475569;&quot;&gt;
        &lt;i class=&quot;fas fa-check-circle&quot; style=&quot;color: #10b981; margin-right: 5px;&quot;&gt;&lt;/i&gt;
        이 이미지 하나만 있으면 똑같은 컴퓨터를 100대든 1000대든 즉시 생성 가능
      &lt;/div&gt;
    &lt;/div&gt;
  &lt;/div&gt;
  &lt;div style=&quot;display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 0.8rem;&quot;&gt;
    &lt;div style=&quot;background: white; border: 1px solid #e2e8f0; border-radius: 0.6rem; padding: 1rem 0.5rem; text-align: center;&quot;&gt;
      &lt;div style=&quot;color: #f59e0b; margin-bottom: 0.3rem;&quot;&gt;&lt;i class=&quot;fas fa-users&quot; style=&quot;font-size: 1.2rem;&quot;&gt;&lt;/i&gt;&lt;/div&gt;
      &lt;strong style=&quot;display: block; font-size: 0.85rem; color: #1e293b; margin-bottom: 0.2rem;&quot;&gt;1. 공용 AMI&lt;/strong&gt;
      &lt;div style=&quot;font-size: 0.75rem; color: #64748b;&quot;&gt;AWS 기본 제공&lt;br /&gt;&lpar;Linux, Windows 등&rpar;&lt;/div&gt;
    &lt;/div&gt;
    &lt;div style=&quot;background: white; border: 1px solid #e2e8f0; border-radius: 0.6rem; padding: 1rem 0.5rem; text-align: center;&quot;&gt;
      &lt;div style=&quot;color: #3b82f6; margin-bottom: 0.3rem;&quot;&gt;&lt;i class=&quot;fas fa-user-cog&quot; style=&quot;font-size: 1.2rem;&quot;&gt;&lt;/i&gt;&lt;/div&gt;
      &lt;strong style=&quot;display: block; font-size: 0.85rem; color: #1e293b; margin-bottom: 0.2rem;&quot;&gt;2. 사용자 정의 AMI&lt;/strong&gt;
      &lt;div style=&quot;font-size: 0.75rem; color: #64748b;&quot;&gt;내가 직접 세팅하고&lt;br /&gt;저장한 나만의 이미지&lt;/div&gt;
    &lt;/div&gt;
    &lt;div style=&quot;background: white; border: 1px solid #e2e8f0; border-radius: 0.6rem; padding: 1rem 0.5rem; text-align: center;&quot;&gt;
      &lt;div style=&quot;color: #10b981; margin-bottom: 0.3rem;&quot;&gt;&lt;i class=&quot;fas fa-shopping-cart&quot; style=&quot;font-size: 1.2rem;&quot;&gt;&lt;/i&gt;&lt;/div&gt;
      &lt;strong style=&quot;display: block; font-size: 0.85rem; color: #1e293b; margin-bottom: 0.2rem;&quot;&gt;3. 마켓플레이스&lt;/strong&gt;
      &lt;div style=&quot;font-size: 0.75rem; color: #64748b;&quot;&gt;검증된 기업의 솔루션&lt;br /&gt;&lpar;구매하여 사용&rpar;&lt;/div&gt;
    &lt;/div&gt;
  &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;

&lt;div class=&quot;story-box&quot;&gt;
  &lt;p&gt;가장 많이 사용하는 방식은 &lt;strong&gt;[사용자 정의 AMI]&lt;/strong&gt;입니다. EC2를 하나 띄워서 필요한 세팅을 완벽하게 끝낸 후, 그것을 본떠서 이미지를 만듭니다. 이때 &lt;strong class=&quot;highlight-text&quot;&gt;데이터 무결성&lpar;Data Integrity&rpar;&lt;/strong&gt;을 위해 인스턴스를 잠시 멈추는 것이 권장됩니다.&lt;/p&gt;
&lt;/div&gt;

&lt;div class=&quot;info-box&quot;&gt;
&lt;div style=&quot;background-color: white; margin-bottom: 2rem; font-family: &#39;Apple SD Gothic Neo&#39;, sans-serif; font-size: 0.85rem; letter-spacing: -0.03em; line-height: 1.4; max-width: 820px; margin-left: auto; margin-right: auto; color: #334155;&quot;&gt;
  &lt;div style=&quot;border: 2px solid #475569; border-radius: 0.8rem; overflow: hidden;&quot;&gt;
    &lt;div style=&quot;background: #475569; color: white; padding: 0.6rem; text-align: center; font-weight: 800; font-size: 0.9rem;&quot;&gt;
      🛠️ AMI 생성 및 활용 과정
    &lt;/div&gt;
    &lt;div style=&quot;display: flex; align-items: stretch; background: white; padding: 1.5rem 1rem; gap: 0.5rem; justify-content: space-between;&quot;&gt;
      &lt;div style=&quot;flex: 1; display: flex; flex-direction: column; align-items: center; text-align: center;&quot;&gt;
        &lt;div style=&quot;background: #eff6ff; color: #3b82f6; width: 40px; height: 40px; border-radius: 50%; display: flex; align-items: center; justify-content: center; margin-bottom: 0.5rem; border: 1px solid #bfdbfe;&quot;&gt;
          &lt;strong style=&quot;font-size: 0.9rem;&quot;&gt;1&lt;/strong&gt;
        &lt;/div&gt;
        &lt;div style=&quot;font-weight: 700; font-size: 0.8rem; color: #334155; margin-bottom: 0.2rem;&quot;&gt;원본 세팅&lt;/div&gt;
        &lt;div style=&quot;font-size: 0.7rem; color: #64748b;&quot;&gt;EC2 시작 후&lt;br /&gt;SW 설치/설정&lt;/div&gt;
      &lt;/div&gt;
      &lt;div style=&quot;display: flex; align-items: center; color: #cbd5e1;&quot;&gt;&lt;i class=&quot;fas fa-chevron-right&quot;&gt;&lt;/i&gt;&lt;/div&gt;
      &lt;div style=&quot;flex: 1; display: flex; flex-direction: column; align-items: center; text-align: center;&quot;&gt;
        &lt;div style=&quot;background: #fef2f2; color: #ef4444; width: 40px; height: 40px; border-radius: 50%; display: flex; align-items: center; justify-content: center; margin-bottom: 0.5rem; border: 1px solid #fecaca;&quot;&gt;
          &lt;strong style=&quot;font-size: 0.9rem;&quot;&gt;2&lt;/strong&gt;
        &lt;/div&gt;
        &lt;div style=&quot;font-weight: 700; font-size: 0.8rem; color: #334155; margin-bottom: 0.2rem;&quot;&gt;인스턴스 중지&lt;/div&gt;
        &lt;div style=&quot;font-size: 0.7rem; color: #64748b;&quot;&gt;파일 손상 방지&lt;br /&gt;&lpar;권장 사항&rpar;&lt;/div&gt;
      &lt;/div&gt;
      &lt;div style=&quot;display: flex; align-items: center; color: #cbd5e1;&quot;&gt;&lt;i class=&quot;fas fa-chevron-right&quot;&gt;&lt;/i&gt;&lt;/div&gt;
      &lt;div style=&quot;flex: 1; display: flex; flex-direction: column; align-items: center; text-align: center;&quot;&gt;
        &lt;div style=&quot;background: #f0fdf4; color: #10b981; width: 40px; height: 40px; border-radius: 50%; display: flex; align-items: center; justify-content: center; margin-bottom: 0.5rem; border: 1px solid #bbf7d0;&quot;&gt;
          &lt;strong style=&quot;font-size: 0.9rem;&quot;&gt;3&lt;/strong&gt;
        &lt;/div&gt;
        &lt;div style=&quot;font-weight: 700; font-size: 0.8rem; color: #334155; margin-bottom: 0.2rem;&quot;&gt;AMI 생성&lt;/div&gt;
        &lt;div style=&quot;font-size: 0.7rem; color: #64748b;&quot;&gt;스냅샷 자동 생성&lt;br /&gt;및 이미지 등록&lt;/div&gt;
      &lt;/div&gt;
      &lt;div style=&quot;display: flex; align-items: center; color: #cbd5e1;&quot;&gt;&lt;i class=&quot;fas fa-chevron-right&quot;&gt;&lt;/i&gt;&lt;/div&gt;
      &lt;div style=&quot;flex: 1; display: flex; flex-direction: column; align-items: center; text-align: center;&quot;&gt;
        &lt;div style=&quot;background: #fffbeb; color: #f59e0b; width: 40px; height: 40px; border-radius: 50%; display: flex; align-items: center; justify-content: center; margin-bottom: 0.5rem; border: 1px solid #fde68a;&quot;&gt;
          &lt;strong style=&quot;font-size: 0.9rem;&quot;&gt;4&lt;/strong&gt;
        &lt;/div&gt;
        &lt;div style=&quot;font-weight: 700; font-size: 0.8rem; color: #334155; margin-bottom: 0.2rem;&quot;&gt;대량 배포&lt;/div&gt;
        &lt;div style=&quot;font-size: 0.7rem; color: #64748b;&quot;&gt;AMI를 사용하여&lt;br /&gt;새 인스턴스 시작&lt;/div&gt;
      &lt;/div&gt;
    &lt;/div&gt;
  &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;

&lt;div class=&quot;story-box&quot; style=&quot;margin-bottom:0&quot;&gt;
  &lt;h4 style=&quot;color: #1e293b; font-weight: 800; margin-bottom: 1rem;&quot;&gt;Q. User Data도 초기 설정을 하잖아요? 뭐가 달라요?&lt;/h4&gt;

  &lt;p&gt;맞습니다. 둘 다 인스턴스를 처음 시작할 때 환경을 구성하는 방법입니다. 가장 큰 차이는 &lt;strong&gt;“설정을 언제 하느냐&lpar;Timing&rpar;”&lt;/strong&gt;입니다.
쉽게 비유하자면 &lt;strong&gt;냉동 피자&lpar;AMI&rpar;&lt;/strong&gt;와 &lt;strong&gt;밀키트&lpar;User Data&rpar;&lt;/strong&gt;의 차이와 같습니다.&lt;/p&gt;
&lt;/div&gt;

&lt;div class=&quot;info-box&quot;&gt;
  &lt;div style=&quot;font-family: &#39;Apple SD Gothic Neo&#39;, sans-serif; font-size: 0.8rem; letter-spacing: -0.03em; line-height: 1.4; margin-left: auto; margin-right: auto; color: #334155;&quot;&gt;
  &lt;div style=&quot;background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 0.6rem; padding: 0.8rem;&quot;&gt;
    &lt;div style=&quot;font-weight: 800; color: #1e293b; margin-bottom: 0.6rem; text-align: center; font-size: 0.85rem;&quot;&gt;
      ⚖️ 기술적 차이점 요약
    &lt;/div&gt;    
    &lt;div style=&quot;display: grid; grid-template-columns: repeat&lpar;4, 1fr&rpar;; gap: 0.4rem; text-align: center;&quot;&gt;
      &lt;div style=&quot;font-weight: 700; color: #64748b; font-size: 0.75rem; padding-bottom: 0.3rem; border-bottom: 1px solid #cbd5e1;&quot;&gt;구분&lt;/div&gt;
      &lt;div style=&quot;font-weight: 700; color: #7c3aed; font-size: 0.75rem; padding-bottom: 0.3rem; border-bottom: 1px solid #a78bfa;&quot;&gt;AMI&lt;/div&gt;
      &lt;div style=&quot;font-weight: 700; color: #2563eb; font-size: 0.75rem; padding-bottom: 0.3rem; border-bottom: 1px solid #93c5fd;&quot;&gt;User Data&lt;/div&gt;
      &lt;div style=&quot;font-weight: 700; color: #059669; font-size: 0.75rem; padding-bottom: 0.3rem; border-bottom: 1px solid #6ee7b7;&quot;&gt;추천&lt;/div&gt;
      &lt;div style=&quot;font-size: 0.75rem; color: #334155; padding: 0.3rem 0; border-bottom: 1px solid #e2e8f0;&quot;&gt;설정 시점&lt;/div&gt;
      &lt;div style=&quot;font-size: 0.75rem; color: #475569; padding: 0.3rem 0; border-bottom: 1px solid #e2e8f0; background: #faf5ff;&quot;&gt;Baking &lpar;생성&rpar;&lt;/div&gt;
      &lt;div style=&quot;font-size: 0.75rem; color: #475569; padding: 0.3rem 0; border-bottom: 1px solid #e2e8f0; background: #eff6ff;&quot;&gt;Boot &lpar;부팅&rpar;&lt;/div&gt;
      &lt;div style=&quot;font-size: 0.7rem; color: #94a3b8; padding: 0.3rem 0; border-bottom: 1px solid #e2e8f0;&quot;&gt;-&lt;/div&gt;
      &lt;div style=&quot;font-size: 0.75rem; color: #334155; padding: 0.3rem 0; border-bottom: 1px solid #e2e8f0;&quot;&gt;부팅 속도&lt;/div&gt;
      &lt;div style=&quot;font-size: 0.75rem; color: #7c3aed; font-weight: 700; padding: 0.3rem 0; border-bottom: 1px solid #e2e8f0; background: #faf5ff;&quot;&gt;빠름 🚀&lt;/div&gt;
      &lt;div style=&quot;font-size: 0.75rem; color: #94a3b8; padding: 0.3rem 0; border-bottom: 1px solid #e2e8f0; background: #eff6ff;&quot;&gt;느림 🐢&lt;/div&gt;
      &lt;div style=&quot;font-size: 0.7rem; color: #64748b; padding: 0.3rem 0; border-bottom: 1px solid #e2e8f0;&quot;&gt;설치 많으면 AMI&lt;/div&gt;
      &lt;div style=&quot;font-size: 0.75rem; color: #334155; padding: 0.3rem 0;&quot;&gt;업데이트&lt;/div&gt;
      &lt;div style=&quot;font-size: 0.75rem; color: #94a3b8; padding: 0.3rem 0; background: #faf5ff;&quot;&gt;어려움&lt;/div&gt;
      &lt;div style=&quot;font-size: 0.75rem; color: #2563eb; font-weight: 700; padding: 0.3rem 0; background: #eff6ff;&quot;&gt;쉬움&lt;/div&gt;
      &lt;div style=&quot;font-size: 0.7rem; color: #64748b; padding: 0.3rem 0;&quot;&gt;잦은 변경 User Data&lt;/div&gt;
    &lt;/div&gt;
  &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;

&lt;div style=&quot;margin-bottom: 1.5rem;&quot;&gt;
  &lt;h4 style=&quot;margin: 0; color: #1e293b; font-weight: 800;&quot;&gt;✔️ 실전 운영 및 시험 포인트 &lpar;Deep Dive&rpar;&lt;/h4&gt;
&lt;/div&gt;

&lt;div class=&quot;deep-dive-list&quot;&gt;

  &lt;div class=&quot;dd-item&quot;&gt;
    &lt;div class=&quot;dd-header&quot;&gt;
      &lt;span class=&quot;dd-title&quot;&gt;1. AMI는 리전&lpar;Region&rpar;에 종속됩니다.&lt;/span&gt;
    &lt;/div&gt;
    &lt;p class=&quot;dd-content&quot;&gt;
      서울 리전&lpar;ap-northeast-2&rpar;에서 만든 AMI는 버지니아 리전&lpar;us-east-1&rpar;에서 바로 보이지 않습니다. 다른 리전에서 사용하려면 &lt;span class=&quot;code-span&quot;&gt;AMI 복사&lpar;Copy AMI&rpar;&lt;/span&gt; 기능을 통해 해당 리전으로 이미지를 복제해야 합니다.
    &lt;/p&gt;
  &lt;/div&gt;

  &lt;div class=&quot;dd-item&quot;&gt;
    &lt;div class=&quot;dd-header&quot;&gt;
      &lt;span class=&quot;dd-title&quot;&gt;2. 실무 권장: 하이브리드 전략 &lpar;Golden Image&rpar;&lt;/span&gt;
      &lt;span class=&quot;dd-badge green&quot;&gt;Best Practice&lt;/span&gt;
    &lt;/div&gt;
    &lt;p class=&quot;dd-content&quot;&gt;
      어느 하나만 쓰기보다는 둘을 섞어 쓰는 것이 좋습니다.

       &lt;div style=&quot;text-align: center; margin-top:1rem; margin-bottom:1rem;&quot;&gt;
          &lt;div style=&quot;display: inline-block; background: #fff; border: 1px dashed #cbd5e1; border-radius: 0.6rem; padding: 0.8rem; width: 100%; box-sizing: border-box;&quot;&gt;
            &lt;strong style=&quot;color: #059669; font-size: 0.85rem;&quot;&gt;💡 실무 Best Practice &lpar;하이브리드 전략&rpar;&lt;/strong&gt;
            &lt;div style=&quot;display: flex; flex-wrap: wrap; align-items: center; justify-content: center; gap: 0.5rem; margin-top: 0.5rem;&quot;&gt;
              &lt;div style=&quot;background: #f5f3ff; color: #7c3aed; padding: 0.2rem 0.5rem; border-radius: 4px; font-size: 0.75rem; border: 1px solid #ddd6fe;&quot;&gt;
                &lt;strong&gt;AMI&lt;/strong&gt; &lpar;무거운 설치&rpar;
              &lt;/div&gt;
              &lt;i class=&quot;fas fa-plus&quot; style=&quot;color: #94a3b8; font-size: 0.7rem;&quot;&gt;&lt;/i&gt;
              &lt;div style=&quot;background: #eff6ff; color: #2563eb; padding: 0.2rem 0.5rem; border-radius: 4px; font-size: 0.75rem; border: 1px solid #bfdbfe;&quot;&gt;
                &lt;strong&gt;User Data&lt;/strong&gt; &lpar;가벼운 설정&rpar;
              &lt;/div&gt;
            &lt;/div&gt;
            &lt;div style=&quot;font-size: 0.75rem; color: #64748b; margin-top: 0.3rem;&quot;&gt;
              = &lt;strong style=&quot;color: #475569;&quot;&gt;Golden Image&lt;/strong&gt; 전략 &lpar;속도와 유연성 모두 확보&rpar;
            &lt;/div&gt;
          &lt;/div&gt;
        &lt;/div&gt;
        
      &lt;span class=&quot;sub-text&quot;&gt;
        • &lt;strong&gt;AMI:&lt;/strong&gt; 설치가 오래 걸리는 OS 패치, DB 엔진 등을 미리 설치&lt;br /&gt;
        • &lt;strong&gt;User Data:&lt;/strong&gt; 자주 바뀌는 설정 파일이나 최신 코드만 부팅 시 다운로드
      &lt;/span&gt;
    &lt;/p&gt;
  &lt;/div&gt;

  &lt;div class=&quot;dd-item&quot;&gt;
    &lt;div class=&quot;dd-header&quot;&gt;
      &lt;span class=&quot;dd-title&quot;&gt;3. AMI 삭제 시 스냅샷도 지워야 합니다.&lt;/span&gt;
      &lt;span class=&quot;dd-badge red&quot;&gt;비용 주의&lt;/span&gt;
    &lt;/div&gt;
    &lt;p class=&quot;dd-content&quot;&gt;
      AMI 등록을 해제&lpar;Deregister&rpar;해도, 원본이 되는 &lt;strong&gt;EBS 스냅샷은 S3에 그대로 남아 과금&lt;/strong&gt;됩니다. 완전히 삭제하려면 AMI 해제 후 스냅샷도 별도로 삭제해야 합니다.
    &lt;/p&gt;
  &lt;/div&gt;

&lt;/div&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;</td></tr><tr><td width='20%'>DATE</td><td width='80%'><a href='https://shinhyeong.github.io/retrospective/2025-aws-hackaton-retrospective/'><b>2025 AWS 해커톤 &lpar;GWNU X KNU&rpar; 회고</b></a><br/>&lt;p&gt;&lt;img src=&quot;https://shinhyeong.github.io/assets/images/2025-11-28-2025-aws-hackaton-retrospective/2025-aws-hackaton-info.jpeg&quot; alt=&quot;2025 AWS Hackathon Info&quot; style=&quot;display: block; margin: 2rem auto; max-width: 90%; height: auto;&quot; /&gt;&lt;/p&gt;

&lt;div style=&quot;max-width: 800px; margin: 1.5rem auto 2.5rem auto; background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 8px; padding: 1rem; text-align: center; color: #334155; font-family: -apple-system, sans-serif;&quot;&gt;
  
  &lt;div style=&quot;display: flex; flex-direction: column; gap: 0.5rem; justify-content: center; align-items: center;&quot;&gt;
    
    &lt;div style=&quot;font-size: 0.95rem; font-weight: 700; color: #1e293b; display: flex; align-items: center; gap: 6px;&quot;&gt;
      &lt;span style=&quot;font-size: 1.1rem;&quot;&gt;🗓️&lt;/span&gt; 2025.11.22 - 2025.11.23 &lt;span style=&quot;font-weight: 400; color: #64748b; font-size: 0.85rem;&quot;&gt;&lpar;무박 2일&rpar;&lt;/span&gt;
    &lt;/div&gt;
    
    &lt;div style=&quot;width: 40px; height: 1px; background: #cbd5e1; margin: 0.2rem 0;&quot;&gt;&lt;/div&gt;

    &lt;div style=&quot;font-size: 0.95rem; font-weight: 700;display: flex; align-items: center; gap: 6px;&quot;&gt;
      &lt;span style=&quot;font-size: 1.1rem;&quot;&gt;✏️&lt;/span&gt; 2025 강릉원주대학교 X 강원대학교 AWS 해커톤
    &lt;/div&gt;

  &lt;/div&gt;

&lt;/div&gt;

&lt;h1 id=&quot;1-아이디어-구상--공급자가-아닌-사용자의-시선으로&quot;&gt;1. 아이디어 구상 : ‘공급자’가 아닌 ‘사용자’의 시선으로&lt;/h1&gt;

&lt;div class=&quot;story-box&quot;&gt;

  &lt;p&gt;솔직히 고백하자면, 해커톤 시작 전엔 내 머릿속엔 ‘수상실적’ 네 글자뿐이었다. 하지만 해커톤 시작 전, 넥스트클라우드 최민철 멘토님의 말씀은 이런 내 마음을 완전히 바꾸었다.&lt;/p&gt;

  &lt;blockquote&gt;
    &lt;p&gt;“’공급자’의 마음가짐으로 개발하면 안됩니다.”&lt;/p&gt;
  &lt;/blockquote&gt;

  &lt;p&gt;멘토님은 개발자가 실제 사용자의 환경&lpar;돈, 시간적 여유 등&rpar;을 고려하지 않고 기능 구현에만 매몰되는 현상을 지적하셨다. ‘자취생 레시피 앱’을 예로 들자면, 자취생들이 요리를 안 하는 건 레시피를 몰라서가 아니라, 돈과 여유가 없어서인데 개발자들은 “기능 좋은 앱을 만들었는데 왜 안 쓰지?”라며 유저 탓을 한다는 것이다. 이렇게 실제 통계와 유저의 상황을 보지 않고 반문하는 것은 &lt;strong class=&quot;highlight-text&quot;&gt;개발자의 아집이나 다름없다&lt;/strong&gt;는 그 말이 마음을 울렸다.&lt;/p&gt;

  &lt;p&gt;이 조언을 기점으로 목표를 수정했다. 수상 여부를 떠나 &lt;strong class=&quot;highlight-text&quot;&gt;“내가 당장 필요하고, 쓰고 싶은 서비스”&lt;/strong&gt;라는 본질에 집중하기로 했다. 그렇게 &lt;strong&gt;FactCheckAI&lt;/strong&gt;를 구상하게 되었다.&lt;/p&gt;

&lt;/div&gt;

&lt;h2 id=&quot;factcheckai--깃허브-코드-기반-자소서-검증-서비스&quot;&gt;&lt;span class=&quot;title-with-dot&quot;&gt;FactCheckAI&lt;/span&gt; &lt;span class=&quot;title-sub-desc&quot;&gt;: 깃허브 코드 기반 자소서 검증 서비스&lt;/span&gt;&lt;/h2&gt;

&lt;div class=&quot;story-box&quot;&gt;

  &lt;p&gt;나는 기술면접을 종종 볼 기회가 있어 LLM으로 면접 예상 질문을 뽑아서 연습한다. 그런데 단순 CS 지식 확인 면접말고 포트폴리오로 진행되는 면접은 매번 여러 개의 코드를 일일이 복사해야하고 LLM 프롬프트 조건을 상세하게 입력해야 한다는 게 매우 번거로웠었다. 그래서 이 불편함을 내가 직접 해결해보고자 이 아이디어를 생각하게 되었다.&lt;/p&gt;

  &lt;p&gt;간단하게 설명하자면, 다음과 같은 핵심 기능을 제공한다.&lt;/p&gt;

  &lt;div class=&quot;info-box&quot;&gt;
&lt;div style=&quot;display: flex; flex-wrap: wrap; gap: 10px; margin-bottom: 1.5rem;&quot;&gt;
    
    &lt;div style=&quot;flex: 1; min-width: 200px; background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 8px; padding: 1rem; text-align: center; color: #1e293b; font-weight: 700; box-shadow: 0 1px 2px rgba&lpar;0,0,0,0.05&rpar;;&quot;&gt;
      🔍&lt;br /&gt;진위 판독
    &lt;/div&gt;

    &lt;div style=&quot;flex: 1; min-width: 200px; background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 8px; padding: 1rem; text-align: center; color: #1e293b; font-weight: 700; box-shadow: 0 1px 2px rgba&lpar;0,0,0,0.05&rpar;;&quot;&gt;
      🤖&lt;br /&gt;맞춤형 질문 생성
    &lt;/div&gt;

    &lt;div style=&quot;flex: 1; min-width: 200px; background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 8px; padding: 1rem; text-align: center; color: #1e293b; font-weight: 700; box-shadow: 0 1px 2px rgba&lpar;0,0,0,0.05&rpar;;&quot;&gt;
      💬&lt;br /&gt;꼬리 질문 심층 면접
    &lt;/div&gt;

  &lt;/div&gt;

  &lt;div style=&quot;color: #334155; line-height: 1.7; margin-bottom: 2rem; padding: 0 5px;&quot;&gt;
    &lt;p style=&quot;margin-bottom: 0.8rem;&quot;&gt;
      &lt;strong&gt;🔍 진위 판독&lt;/strong&gt;
      &lt;p style=&quot;padding-left:2rem;&quot;&gt;&quot;자소서엔 있는데 코드엔 없다?&quot;&lt;br /&gt;지원자의 주장과 깃허브 코드를 대조해 구현 여부를 4단계로 꼼꼼하게 검증함.&lt;/p&gt;
    &lt;/p&gt;
    &lt;p style=&quot;margin-bottom: 0.8rem;&quot;&gt;
      &lt;strong&gt;🤖 맞춤형 질문 생성&lt;/strong&gt;&lt;br /&gt;
      &lt;p style=&quot;padding-left:2rem;&quot;&gt;단순한 공통 질문이 아니라, JD&lpar;직무 기술서&rpar;와 제출된 코드를 정밀 분석해&lt;br /&gt;면접관이 던질 법한 날카로운 질문을 생성함.&lt;/p&gt;
    &lt;/p&gt;
    &lt;p style=&quot;margin-bottom: 0;&quot;&gt;
      &lt;strong&gt;💬 심층 면접 시뮬레이션&lt;/strong&gt;&lt;br /&gt;
      &lt;p style=&quot;padding-left:2rem;&quot;&gt;단답형 답변으로 끝나지 않도록, 꼬리물기 질문을 계속 던져&lt;br /&gt;실전 압박 면접을 완벽하게 대비할 수 있음.&lt;/p&gt;
    &lt;/p&gt;
  &lt;/div&gt;
  
&lt;/div&gt;

  &lt;div style=&quot;display: flex; flex-wrap: wrap; gap: 10px;&quot;&gt;
  
  &lt;a href=&quot;https://github.com/saa-hackathon-2025/factcheck&quot; target=&quot;_blank&quot; style=&quot;flex: 1; min-width: 250px; text-decoration: none; display: flex; align-items: center; justify-content: space-between; background: #fff; border: 1px solid #cbd5e1; border-radius: 6px; padding: 0.7rem 1rem; transition: background 0.2s;&quot;&gt;
    &lt;div style=&quot;display: flex; flex-direction: column;&quot;&gt;
      &lt;span style=&quot;font-size: 0.9rem; font-weight: 700; color: #1e293b;&quot;&gt;🚀 Final Version&lt;/span&gt;
      &lt;span style=&quot;font-size: 0.75rem; color: #64748b;&quot;&gt;최종 제출 버전 &lpar;Submission&rpar;&lt;/span&gt;
    &lt;/div&gt;
    &lt;div style=&quot;font-size: 1rem; color: #94a3b8;&quot;&gt;↗&lt;/div&gt;
  &lt;/a&gt;

&lt;/div&gt;
&lt;/div&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;h1 id=&quot;2-잘했던-점keep--과거의-실패를-철저한-준비로&quot;&gt;2. 잘했던 점&lpar;Keep&rpar; : 과거의 실패를 ‘철저한 준비’로&lt;/h1&gt;

&lt;div class=&quot;story-box&quot;&gt;

  &lt;p&gt;팀 내 아이디어 회의 끝에, 2가지 후보로 추려졌다.&lt;/p&gt;

  &lt;div style=&quot;font-family: &#39;Apple SD Gothic Neo&#39;, sans-serif; font-size: 0.8rem; letter-spacing: -0.03em; line-height: 1.4; max-width: 800px; margin: 1.5rem auto; color: #334155;&quot;&gt;

  &lt;div style=&quot;background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 0.6rem; padding: 0.8rem;&quot;&gt;
    &lt;div style=&quot;font-weight: 800; color: #1e293b; margin-bottom: 0.8rem; text-align: center; font-size: 0.9rem;&quot;&gt;
      ⚖️ 아이디어 선정 기준 비교
    &lt;/div&gt;
    
    &lt;div style=&quot;display: grid; grid-template-columns: 1.2fr 1fr 1fr; gap: 0.4rem; text-align: center; align-items: stretch;&quot;&gt;
      
      &lt;div style=&quot;font-weight: 700; color: #64748b; font-size: 0.75rem; padding-bottom: 0.4rem; border-bottom: 2px solid #cbd5e1;&quot;&gt;아이디어&lt;/div&gt;
      &lt;div style=&quot;font-weight: 700; color: #64748b; font-size: 0.75rem; padding-bottom: 0.4rem; border-bottom: 2px solid #cbd5e1;&quot;&gt;이전 수상 사례&lt;/div&gt;
      &lt;div style=&quot;font-weight: 700; color: #64748b; font-size: 0.75rem; padding-bottom: 0.4rem; border-bottom: 2px solid #cbd5e1;&quot;&gt;13시간 내 구현&lt;/div&gt;

      &lt;div style=&quot;font-size: 0.75rem; color: #334155; padding: 0.8rem 0.4rem; display: flex; align-items: center; justify-content: center; flex-direction: column; border-radius: 4px 0 0 4px;&quot;&gt;
        &lt;strong&gt;사기탐지 AI&lt;/strong&gt;
        &lt;span style=&quot;color:#64748b; font-size:0.9em; margin-top:2px;&quot;&gt;&lpar;이미지, 피싱&rpar;&lt;/span&gt;
      &lt;/div&gt;
      &lt;div style=&quot;font-size: 0.75rem; color: #475569; padding: 0.8rem 0.4rem; display: flex; align-items: center; justify-content: center;&quot;&gt;
        🟢 많음 &lpar;6건&rpar;
      &lt;/div&gt;
      &lt;div style=&quot;font-size: 0.75rem; color: #475569; padding: 0.8rem 0.4rem; display: flex; align-items: center; justify-content: center; border-radius: 0 4px 4px 0;&quot;&gt;
        🟢 이전 해커톤 수상 사례가&lt;br /&gt;많으니 가능할지도..?
      &lt;/div&gt;

      &lt;div style=&quot;font-size: 0.75rem; color: #1e3a8a; padding: 0.8rem 0.4rem; background: #eff6ff; display: flex; align-items: center; justify-content: center; flex-direction: column; font-weight: 700; border-radius: 4px 0 0 4px;&quot;&gt;
        자소서 검증
        &lt;span style=&quot;color:#3b82f6; font-size:0.9em; margin-top:2px; font-weight:400;&quot;&gt;&lpar;내 아이디어&rpar;&lt;/span&gt;
      &lt;/div&gt;
      &lt;div style=&quot;font-size: 0.75rem; color: #1e40af; padding: 0.8rem 0.4rem; background: #eff6ff; display: flex; align-items: center; justify-content: center; font-weight: 500;&quot;&gt;
        🔺 적음 &lpar;2건&rpar;
      &lt;/div&gt;
      &lt;div style=&quot;font-size: 0.75rem; color: #1e40af; padding: 0.8rem 0.4rem; background: #eff6ff; display: flex; align-items: center; justify-content: center; font-weight: 800; border-radius: 0 4px 4px 0;&quot;&gt;
        🔺 미지수 &lpar;애매함&rpar;
      &lt;/div&gt;

    &lt;/div&gt;
  &lt;/div&gt;
&lt;/div&gt;

  &lt;p&gt;사기 탐지 AI는 구현이 쉽지만, 이미 대기업도 개발중인 서비스라 차별성이 부족했다. 내 아이디어는 매력적이라는 평을 받았지만 &lt;strong&gt;‘13시간 내 구현 가능성’&lt;/strong&gt;이 미지수였다. 나 스스로도 13시간 내로 구현이 가능할지 확신이 없었다.&lt;/p&gt;

  &lt;p&gt;2년 전, ‘2023 SW중심대학 해커톤’이라는 전국 단위 해커톤에 참가했을 때 악몽이 떠올랐다. 아이디어 스펙을 욕심낸 탓에 개발 시간이 부족했고, 그 시간을 벌기 위해 무리하게 밤을 새우다 보니 컨디션 난조로 개발 속도가 오히려 더뎌지는 악순환을 겪었다. 아이디어를 축소시켜 겨우 기능은 구현했지만 발표 무대에서는 체력 저하로 준비한 만큼의 역량을 보여주지 못해 크게 아쉬움이 남았었다. 이번 해커톤은 &lt;strong class=&quot;highlight-text&quot;&gt;기술적 불확실성을 미리 제거&lt;/strong&gt;함으로써 절대 무리하고 싶지 않았다. 해커톤을 즐기고 싶었다.&lt;/p&gt;

  &lt;p&gt;그래서 나는 &lt;strong class=&quot;highlight-text&quot;&gt;가장 구현이 까다로운 핵심 기능들을 미리 프로토타이핑&lt;/strong&gt;해봄으로써 나 스스로도 확신을 얻고, 팀원 또한 설득시키고자 했다. 다행히 프로토타이핑은 성공했고 그렇게 나의 아이디어가 최종 선정되었다.&lt;/p&gt;

  &lt;p&gt;이 선택은 의외로 우리 팀의 &lt;strong&gt;강력한 심리적 안전장치&lt;/strong&gt;가 되기도 했다. 해커톤 초반, 다른 팀들이 기술 스택을 정하고 아이디어 브레인 스토밍을 하느라 우왕좌왕할 때, 우리는 빠르게 핵심 기능을 개발하고, QA와 서비스의 완성도를 높이는 데 온전히 집중할 수 있었다. &lt;strong class=&quot;highlight-text&quot;&gt;과거의 실패가 전화위복이 되어 우리 팀의 큰 경쟁력이 된 순간이었다.&lt;/strong&gt;&lt;/p&gt;

&lt;/div&gt;

&lt;div class=&quot;icon-box&quot;&gt;
  &lt;div style=&quot;display: flex; flex-wrap: wrap; gap: 10px;&quot;&gt;
    
    &lt;a href=&quot;https://github.com/ShinHyeong/FactCheckAi&quot; target=&quot;_blank&quot; style=&quot;flex: 1; min-width: 250px; text-decoration: none; display: flex; align-items: center; justify-content: space-between; border: 1px solid #cbd5e1; border-radius: 6px; padding: 0.7rem 1rem; transition: all 0.2s ease-in-out;&quot;&gt;
      &lt;div class=&quot;btn-text-group&quot; style=&quot;display: flex; flex-direction: column;&quot;&gt;
        &lt;span class=&quot;btn-title&quot; style=&quot;font-size: 0.9rem; font-weight: 700; color: #1e293b;&quot;&gt;🧪 MVP Version&lt;/span&gt;
        &lt;span class=&quot;btn-sub&quot; style=&quot;font-size: 0.75rem; color: #64748b;&quot;&gt;초기 프로토타입 &lpar;Prototype&rpar;&lt;/span&gt;
      &lt;/div&gt;
      &lt;div class=&quot;btn-icon&quot; style=&quot;font-size: 1rem; color: #94a3b8;&quot;&gt;↗&lt;/div&gt;
    &lt;/a&gt;

  &lt;/div&gt;
&lt;/div&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;h1 id=&quot;3-아쉬웠던-점problem--말-대신-ppt에-친절함을&quot;&gt;3. 아쉬웠던 점&lpar;Problem&rpar; : 말 대신 PPT에 친절함을&lt;/h1&gt;

&lt;p&gt;&lt;img src=&quot;https://shinhyeong.github.io/assets/images/2025-11-28-2025-aws-hackaton-retrospective/2025-aws-hackaton-speech.jpeg&quot; alt=&quot;2025 AWS Hackathon Speech&quot; style=&quot;display: block; margin: 2rem auto; max-width: 70%; height: auto;&quot; /&gt;&lt;/p&gt;

&lt;div class=&quot;story-box&quot;&gt;

  &lt;p&gt;그렇다고 모든 과정이 계획대로 흘러간 것은 아니었다. 앞서 말한 선택 덕분에 핵심 기능 구현은 예상보다 훨씬 빠르게 끝났다. 그러나 발표 준비 과정에서 완벽히 모든 것을 설명하려고 했다. 아이디어 멘토링 시간에 날카로운 질문을 받고 난 후, 나의 설명이 부족하여 우리 서비스의 &lt;strong&gt;핵심 타겟과 차별점이 충분히 전달되지 못할까봐&lt;/strong&gt; 불안해졌기 때문이다.&lt;/p&gt;

  &lt;p&gt;그래서 나는 초등학생이 들어도 단번에 이해할 수 있도록, &lt;strong&gt;대본을 더 세세하고 꼼꼼하게 풀어썼다.&lt;/strong&gt; 원래는 새벽 3시에 컨디션 조절을 위해 잠들 계획이었으나, 이 방대해진 대본을 다듬느라 결국 밤을 새우고 말았다. 그래도 내용을 온전히 전달할 수만 있다면 컨디션이 나빠지는 것은 감수할 수 있었다.&lt;/p&gt;

  &lt;p&gt;하지만 다음 날 현장에서 주어진 발표 시간은 단 &lt;strong&gt;6분&lt;/strong&gt;이었다. 리허설을 해보면서 준비한 내용을 다 설명할 시간은 없음을 직감했다. 결국 밤새 준비한 대본의 절반 이상을 즉석에서 생략하고 넘어가야 했다. 나의 설명이 중간중간 생략되자 심사위원과 청중의 시선은 자연스럽게 발표 자료&lpar;PPT&rpar;로 쏠렸다.&lt;/p&gt;

  &lt;p&gt;발표가 끝난 직후, 발표 준비 전략에 대한 아쉬움이 크게 남았다. 발표시간이 생각보다 짧게 주어질 수 있다는 변수를 생각하지 못했다. 대본에 담으려던 그 친절한 설명을 PPT 안에 녹여냈어야 했다. &lt;strong class=&quot;highlight-text&quot;&gt;설명이 빨라지거나 생략되는 변수 속에서도, PPT만 보면 의문점이 해결될 수 있도록&lt;/strong&gt; 말이다.&lt;/p&gt;

  &lt;p&gt;PPT는 핵심만 간결하게 만들었는데, 정작 준비한 설명을 다 못 하게 되니 불친절한 자료가 되어버린 것 같았다. 제한된 시간 내에 청중을 설득해야 할 경우, 현장 상황에 따라 생략될 수 있는 구두 설명보다는, &lt;strong class=&quot;highlight-text&quot;&gt;청중이 언제든 눈으로 다시 확인할 수 있는 PPT 자체에 상세한 맥락을 담아두는 것&lt;/strong&gt;이 훨씬 안전하고 효과적인 전략임을 깨달았다.&lt;/p&gt;

&lt;/div&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;h1 id=&quot;4-깨달음insight--진심이-만든-비즈니스-경쟁력&quot;&gt;4. 깨달음&lpar;Insight&rpar; : ‘진심’이 만든 ‘비즈니스 경쟁력’&lt;/h1&gt;

&lt;p&gt;&lt;img src=&quot;https://shinhyeong.github.io/assets/images/2025-11-28-2025-aws-hackaton-retrospective/2025-aws-hackaton-final-rank.png&quot; alt=&quot;2025 AWS Hackathon Final Rank&quot; style=&quot;display: block; margin: 2rem auto; max-width: 70%; height: auto;&quot; /&gt;&lt;/p&gt;

&lt;div class=&quot;story-box&quot;&gt;

  &lt;p&gt;발표에 개인적인 아쉬움이 남았지만, 서비스 자체의 완성도와 차별점은 충분히 전달되었다. 결과적으로 우리 팀은 3등&lpar;우수상&rpar;이라는 값진 성과를 거두었다. 수상할 수 있었던 이유는 우리가 이 서비스의 &lt;strong class=&quot;highlight-text&quot;&gt;잠재적 고객&lt;/strong&gt;이었기 때문이라고 생각한다.&lt;/p&gt;

  &lt;p&gt;아이디어 멘토링 시간, 멘토님들은 데모 영상을 보자 “지원자뿐만 아니라 채용 담당자 입장에서도 탐낼 만한 아이디어”라며 가능성을 먼저 인정해 주셨다. 하지만 칭찬도 잠시, 곧이어 서비스의 본질을 꿰뚫는 날카로운 질문이 시작되었다.&lt;/p&gt;

  &lt;blockquote&gt;
    &lt;p&gt;“굳이 이 서비스 안 쓰고 ChatGPT 쓰면 될 것 같은데.. 뭐가 달라요?”
&lt;br /&gt;“이 서비스를 정말로 사람들이 결제할까요? 수익화 전략은 뭐에요?”&lt;/p&gt;
  &lt;/blockquote&gt;

  &lt;p&gt;쏟아지는 질문에 긴장은 되었지만 막힘없이 답변했다. 직접 서비스를 이용할 당사자의 입장에서, 기존 서비스와는 무엇이 달라서 꼭 써야만 하는지, 그리고 어느 지점에서 기꺼이 지갑을 열게 될지를 누구보다 현실적으로 알고 있었기 때문이다.&lt;/p&gt;

  &lt;p&gt;하지만 동시에 멘토님들의 질문을 통해, &lt;strong&gt;우리 서비스의 차별점이 충분히 전달되지 않았음&lt;/strong&gt;을 깨달았다. 나는 당황하는 대신 부족했던 설명을 보충하여 차분히 다시 전달했고, 그제야 멘토님은 고개를 끄덕이셨다. 우리는 이 과정을 놓치지 않고, 다음날 최종 발표에서 논리를 탄탄하게 보강하는 재료로 삼았다.&lt;/p&gt;

  &lt;p&gt;이런 과정을 거치며 비로소 우리가 만든 서비스의 강점이 더 또렷해졌다. 그리고 단순히 아이디어를 설명하는 수준을 넘어 설득력 있는 형태로 다듬어졌다. 우리는 심사위원들의 공감을 이끌어내며 ‘우수상’이라는 결실을 맺을 수 있었다.&lt;/p&gt;

&lt;/div&gt;

&lt;p&gt;&lt;img src=&quot;https://shinhyeong.github.io/assets/images/2025-11-28-2025-aws-hackaton-retrospective/2025-aws-hackaton-team-photo.jpeg&quot; alt=&quot;2025 AWS Hackathon Team Photo&quot; style=&quot;display: block; margin: 2rem auto; max-width: 70%; height: auto;&quot; /&gt;&lt;/p&gt;

&lt;div class=&quot;story-box&quot;&gt;

  &lt;p&gt;이번 해커톤의 가장 큰 수확은 수상 실적 그 자체가 아니다. “어차피 내가 사용할 서비스니까, 기왕 만드는 거 제대로 만들어보자”는 마음으로 치열하게 고민했을 뿐인데, &lt;strong class=&quot;highlight-text&quot;&gt;감사하게도 수상이라는 결과가 뒤따라왔다.&lt;/strong&gt; 이번 수상은 진심을 다해 문제에 파고들면 성과는 자연스럽게 따라온다는 사실을 일깨워 준 뜻깊은 경험이었다.&lt;/p&gt;

  &lt;p&gt;나는 앞으로도 &lt;strong class=&quot;highlight-text&quot;&gt;‘내 코드가 누군가의 문제를 실질적으로 해결해주고 있는지’&lt;/strong&gt; 끊임없이 되물으며, 계속해서 성장해 나갈 것이다.&lt;/p&gt;

&lt;/div&gt;

&lt;div class=&quot;icon-box&quot;&gt;
    &lt;div style=&quot;display: flex; flex-wrap: wrap; gap: 10px;&quot;&gt;
      
      &lt;a href=&quot;https://mandusitstudy.tistory.com/532&quot; target=&quot;_blank&quot; style=&quot;flex: 1; min-width: 250px; text-decoration: none; display: flex; align-items: center; justify-content: space-between; background: #fff; border: 1px solid #cbd5e1; border-radius: 6px; padding: 0.7rem 1rem; transition: background 0.2s;&quot;&gt;
        &lt;div style=&quot;display: flex; flex-direction: column;&quot;&gt;
          &lt;span style=&quot;font-size: 0.9rem; font-weight: 700; color: #1e293b;&quot;&gt;📝 다른 팀원의 후기도 궁금하다면&lt;/span&gt;
          &lt;span style=&quot;font-size: 0.75rem; color: #64748b;&quot;&gt;&lt;/span&gt;
        &lt;/div&gt;
        &lt;div style=&quot;font-size: 1rem; color: #94a3b8;&quot;&gt;↗&lt;/div&gt;
      &lt;/a&gt;

    &lt;/div&gt;
  &lt;/div&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;</td></tr><tr><td width='20%'>DATE</td><td width='80%'><a href='https://shinhyeong.github.io/java/static-methods-advantages-and-disadvantages/'><b>Static 메소드의 장단점</b></a><br/>&lt;h1 id=&quot;static-메소드의-장단점&quot;&gt;Static 메소드의 장단점&lt;/h1&gt;

&lt;h2 id=&quot;장점--효율적인-공유와-편의성&quot;&gt;장점 &lt;span class=&quot;title-sub-desc&quot;&gt;: 효율적인 공유와 편의성&lt;/span&gt;&lt;/h2&gt;

&lt;div class=&quot;info-box&quot; style=&quot;display: flex; gap: 20px; flex-wrap: wrap; background-color: #f8f9fa; border-radius: 12px; padding: 30px; box-shadow: 0 4px 20px rgba&lpar;0,0,0,0.05&rpar;; color: #333;&quot;&gt;
      
      &lt;div style=&quot;flex: 1; min-width: 300px; background: #fff; border-radius: 12px; padding: 25px; box-shadow: 0 4px 15px rgba&lpar;52, 152, 219, 0.1&rpar;;&quot;&gt;
        &lt;h4 style=&quot;margin: 0 0 20px 0; font-size: 16px; color: #2980b9; font-weight: 700;&quot;&gt;1. 객체 생성 없는 &#39;즉시 호출&#39;&lt;/h4&gt;
        
        &lt;div style=&quot;display: flex; align-items: center; justify-content: space-between; gap: 10px;&quot;&gt;
          &lt;div style=&quot;text-align: center; opacity: 0.5;&quot;&gt;
            &lt;div style=&quot;font-size: 11px; text-decoration: line-through;&quot;&gt;new Object&lpar;&rpar;&lt;/div&gt;
            &lt;div style=&quot;font-size: 12px; margin-top: 4px;&quot;&gt;🐢 생성필요&lt;/div&gt;
          &lt;/div&gt;
          
          &lt;div style=&quot;font-size: 12px; color: #ccc;&quot;&gt;vs&lt;/div&gt;

          &lt;div style=&quot;flex: 1; background: #f0f9ff; border-radius: 12px; padding: 12px; text-align: center;&quot;&gt;
            &lt;div style=&quot;font-size: 24px; margin-bottom: 4px;&quot;&gt;⚡️&lt;/div&gt;
            &lt;div style=&quot;font-size: 13px; font-weight: 800; color: #0077d4;&quot;&gt;Class.method&lpar;&rpar;&lt;/div&gt;
            &lt;div style=&quot;font-size: 11px; color: #0077d4; margin-top: 4px;&quot;&gt;바로 실행&lt;/div&gt;
          &lt;/div&gt;
        &lt;/div&gt;
      &lt;/div&gt;

      &lt;div style=&quot;flex: 1; min-width: 300px; background: #fff; border-radius: 12px; padding: 25px; box-shadow: 0 4px 15px rgba&lpar;52, 152, 219, 0.1&rpar;;&quot;&gt;
        &lt;h4 style=&quot;margin: 0 0 20px 0; font-size: 16px; color: #2980b9; font-weight: 700;&quot;&gt;2. 메모리 효율 &lpar;1회 로드&rpar;&lt;/h4&gt;
        
        &lt;div style=&quot;display: flex; align-items: center; justify-content: center; gap: 15px;&quot;&gt;
          &lt;div style=&quot;text-align: center;&quot;&gt;
            &lt;div style=&quot;background: #fff; border: 2px solid #2980b9; padding: 8px 12px; border-radius: 8px; color: #2980b9; font-weight: bold; font-size: 12px;&quot;&gt;
              💾 1개
            &lt;/div&gt;
            &lt;div style=&quot;font-size: 10px; color: #999; margin-top: 4px;&quot;&gt;Method Area&lt;/div&gt;
          &lt;/div&gt;

          &lt;div style=&quot;color: #2980b9;&quot;&gt;◀️&lt;/div&gt;

          &lt;div style=&quot;display: flex; flex-direction: column; gap: 6px;&quot;&gt;
            &lt;div style=&quot;font-size: 11px; color: #555; background: #f0f9ff; padding: 3px 8px; border-radius: 4px; border: 1px solid #dbeafe;&quot;&gt;객체 A&lt;/div&gt;
            &lt;div style=&quot;font-size: 11px; color: #555; background: #f0f9ff; padding: 3px 8px; border-radius: 4px; border: 1px solid #dbeafe;&quot;&gt;객체 B&lt;/div&gt;
            &lt;div style=&quot;font-size: 11px; color: #555; background: #f0f9ff; padding: 3px 8px; border-radius: 4px; border: 1px solid #dbeafe;&quot;&gt;객체 C&lt;/div&gt;
          &lt;/div&gt;
        &lt;/div&gt;
        &lt;div style=&quot;text-align: center; margin-top: 15px; font-size: 12px; color: #7f8c8d;&quot;&gt;모든 객체가 하나를 공유함&lt;/div&gt;
      &lt;/div&gt;

    &lt;/div&gt;

&lt;div class=&quot;story-box&quot;&gt;

  &lt;h3 id=&quot;section&quot;&gt;1&rpar; 객체 생성 없이 사용하는 편리함&lt;/h3&gt;
  &lt;p&gt;Static 메소드의 가장 큰 특징은 &lt;strong class=&quot;highlight-text&quot;&gt;인스턴스&lpar;객체&rpar;를 생성하지 않고도 호출할 수 있다&lt;/strong&gt;는 점입니다. &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Math.abs&lpar;&rpar;&lt;/code&gt;나 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;LocalDate.now&lpar;&rpar;&lt;/code&gt; 처럼, 객체의 상태와 무관하게 입력값만 있으면 결과를 내놓는 &lt;strong&gt;유틸리티성 기능&lt;/strong&gt;을 구현할 때 매우 유용합니다. 불필요한 객체 생성을 줄여 코드를 간결하게 만들어 줍니다.&lt;/p&gt;

  &lt;h3 id=&quot;section-1&quot;&gt;2&rpar; 메모리 효율성&lt;/h3&gt;
  &lt;p&gt;일반적인 메소드는 객체를 생성할 때마다 힙&lpar;Heap&rpar; 영역에 메모리가 할당되지만, Static 메소드는 프로그램이 시작될 때 &lt;strong class=&quot;highlight-text&quot;&gt;메소드 영역&lpar;Method Area&rpar;에 단 한 번만 로드&lt;/strong&gt;됩니다. 모든 객체가 이 하나의 메소드를 공유하므로, 똑같은 기능을 위해 매번 메모리를 소비하는 비효율을 막을 수 있습니다.&lt;/p&gt;

&lt;/div&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;h2 id=&quot;단점--유연성-저하와-메모리-이슈&quot;&gt;단점 &lt;span class=&quot;title-sub-desc&quot;&gt;: 유연성 저하와 메모리 이슈&lt;/span&gt;&lt;/h2&gt;

&lt;div class=&quot;info-box&quot; style=&quot;display: grid; grid-template-columns: repeat&lpar;auto-fit, minmax&lpar;280px, 1fr&rpar;&rpar;; gap: 20px; background-color: #f8f9fa; border-radius: 12px; padding: 30px; box-shadow: 0 4px 20px rgba&lpar;0,0,0,0.05&rpar;; color: #333;&quot;&gt;

      &lt;div style=&quot;background: #fff; border-radius: 12px; padding: 25px; box-shadow: 0 4px 15px rgba&lpar;231, 76, 60, 0.1&rpar;; display: flex; flex-direction: column;&quot;&gt;
        &lt;h4 style=&quot;margin: 0 0 15px 0; font-size: 15px; color: #c0392b; font-weight: 700;&quot;&gt;1. 초기 로딩 부담&lt;/h4&gt;
        
        &lt;div style=&quot;text-align: center; padding: 5px 0; flex: 1; display: flex; flex-direction: column; justify-content: center;&quot;&gt;
          &lt;div style=&quot;display: flex; align-items: center; justify-content: center; gap: 5px; margin-bottom: 5px;&quot;&gt;
             &lt;div style=&quot;font-size: 10px; color: #555;&quot;&gt;Start 🚀&lt;/div&gt;
             &lt;div style=&quot;font-size: 12px; color: #aaa;&quot;&gt;➡️&lt;/div&gt;
             
             &lt;div style=&quot;background: #fff5f5; border: 1px solid #e74c3c; border-radius: 8px; padding: 10px; width: 160px;&quot;&gt;
                &lt;div style=&quot;font-size: 9px; color: #c0392b; font-weight: bold; margin-bottom: 4px;&quot;&gt;Method Area&lt;/div&gt;
                &lt;div style=&quot;background: #e74c3c; color: #fff; font-size: 9px; padding: 6px 2px; border-radius: 4px; font-weight: bold;&quot;&gt;Huge Static&lt;br /&gt;Block 📦&lt;/div&gt;
             &lt;/div&gt;
          &lt;/div&gt;
          
          &lt;div style=&quot;font-size: 11px; color: #c0392b; margin-top: 5px; font-weight: bold;&quot;&gt;🐢 로딩 지연 발생&lt;/div&gt;

          &lt;p style=&quot;margin: 15px 0 0 0; font-size: 12px; color: #999; line-height: 1.4;&quot;&gt;
            프로그램 시작 시 Method Area에&lt;br /&gt;모든 Static 데이터를 한 번에 밀어넣어&lt;br /&gt;
부팅 속도가 느려질 수 있음
          &lt;/p&gt;
        &lt;/div&gt;
      &lt;/div&gt;

      &lt;div style=&quot;background: #fff; border-radius: 12px; padding: 25px; box-shadow: 0 4px 15px rgba&lpar;231, 76, 60, 0.1&rpar;; display: flex; flex-direction: column;&quot;&gt;
        &lt;h4 style=&quot;margin: 0 0 15px 0; font-size: 15px; color: #c0392b; font-weight: 700;&quot;&gt;2. GC 불가 &lpar;메모리 해제 안 됨&rpar;&lt;/h4&gt;
        
        &lt;div style=&quot;text-align: center; padding: 5px 0; flex: 1; display: flex; flex-direction: column; justify-content: center;&quot;&gt;
          
          &lt;div style=&quot;background: #fff5f5; border: 1px solid #e74c3c; border-radius: 6px; padding: 6px; width: 90%; margin: 0 auto;&quot;&gt;
             &lt;div style=&quot;font-size: 9px; color: #c0392b; font-weight: bold; margin-bottom: 2px;&quot;&gt;Method Area&lt;/div&gt;
             &lt;div style=&quot;display: flex; align-items: center; justify-content: center; gap: 5px;&quot;&gt;
               &lt;span style=&quot;font-size: 18px;&quot;&gt;📦 🔒&lt;/span&gt;
               &lt;span style=&quot;font-size: 10px; color: #c0392b; font-weight: bold;&quot;&gt;&lpar;앱 종료 시까지&rpar;&lt;/span&gt;
             &lt;/div&gt;
          &lt;/div&gt;

          &lt;div style=&quot;height: 15px;&quot;&gt;&lt;/div&gt; &lt;div style=&quot;background: #f0f9ff; border: 1px dashed #aaa; border-radius: 6px; padding: 6px; width: 90%; margin: 0 auto; opacity: 0.7;&quot;&gt;
             &lt;div style=&quot;font-size: 9px; color: #555; margin-bottom: 2px;&quot;&gt;Heap Area&lt;/div&gt;
             &lt;div style=&quot;display: flex; align-items: center; justify-content: center; gap: 5px;&quot;&gt;
               &lt;span style=&quot;font-size: 18px;&quot;&gt;🚛 ♻️&lt;/span&gt;
               &lt;span style=&quot;font-size: 10px; color: #555;&quot;&gt;&lpar;GC 가능&rpar;&lt;/span&gt;
             &lt;/div&gt;
          &lt;/div&gt;

          &lt;p style=&quot;margin: 12px 0 0 0; font-size: 12px; color: #999; line-height: 1.4;&quot;&gt;
            필요 없어져도 GC가 수거하지 않음&lt;br /&gt;&lpar;프로그램 종료 전까지 계속 남아있음&rpar;
          &lt;/p&gt;
        &lt;/div&gt;
      &lt;/div&gt;
      
      &lt;div style=&quot;background: #fff; border-radius: 12px; padding: 25px; box-shadow: 0 4px 15px rgba&lpar;231, 76, 60, 0.1&rpar;; display: flex; flex-direction: column;&quot;&gt;
        &lt;h4 style=&quot;margin: 0 0 20px 0; font-size: 15px; color: #c0392b; font-weight: 700;&quot;&gt;3. 인스턴스 변수 접근 불가&lt;/h4&gt;
        
        &lt;div style=&quot;text-align: center; padding: 5px 0; flex: 1; display: flex; flex-direction: column; justify-content: center;&quot;&gt;
          
          &lt;div style=&quot;background: #fff; border: 2px solid #c0392b; border-radius: 6px; padding: 4px; width: 80%; margin: 0 auto;&quot;&gt;
            &lt;div style=&quot;font-size: 9px; font-weight: bold; color: #c0392b;&quot;&gt;[Method Area] static method&lpar;&rpar;&lt;/div&gt;
          &lt;/div&gt;

          &lt;div style=&quot;color: #c0392b; font-weight: bold; font-size: 14px; line-height: 1; margin: 20px 0;&quot;&gt;⬇️ ❌ &lpar;참조 없음&rpar;&lt;/div&gt;

          &lt;div style=&quot;background: #f9f9f9; border: 1px dashed #999; border-radius: 6px; padding: 4px; width: 80%; margin: 0 auto;&quot;&gt;
             &lt;div style=&quot;font-size: 9px; color: #777;&quot;&gt;[Heap Area] this.variable&lt;/div&gt;
          &lt;/div&gt;

          &lt;p style=&quot;margin: 15px 0 0 0; font-size: 12px; color: #999; line-height: 1.4;&quot;&gt;
            메모리 영역이 달라서&lt;br /&gt;객체&lpar;Heap&rpar;의 변수를 볼 수 없음
          &lt;/p&gt;
        &lt;/div&gt;
      &lt;/div&gt;

      &lt;div style=&quot;background: #fff;border-radius: 12px; padding: 25px; box-shadow: 0 4px 15px rgba&lpar;231, 76, 60, 0.1&rpar;;&quot;&gt;
        &lt;h4 style=&quot;margin: 0 0 15px 0; font-size: 15px; color: #c0392b; font-weight: 700;&quot;&gt;4. 오버라이딩 불가&lt;/h4&gt;
        
        &lt;div style=&quot;text-align: center; padding: 5px 0;&quot;&gt;
          &lt;div style=&quot;background: #f8f9fa; border: 1px solid #eee; padding: 6px; border-radius: 4px; font-family: monospace; font-size: 11px; color: #555; margin-bottom: 10px;&quot;&gt;
            &lt;span style=&quot;color: #c0392b; font-weight: bold;&quot;&gt;Parent&lt;/span&gt; p = new Child&lpar;&rpar;;
          &lt;/div&gt;

          &lt;div style=&quot;display: flex; gap: 10px; justify-content: center; align-items: stretch; margin-bottom: 10px;&quot;&gt;
            &lt;div style=&quot;flex: 1; border: 1px solid #c0392b; background: #fff5f5; border-radius: 6px; padding: 6px;&quot;&gt;
               &lt;div style=&quot;font-size: 9px; color: #c0392b; font-weight: bold;&quot;&gt;Compile Time&lt;/div&gt;
               &lt;div style=&quot;font-size: 18px; margin: 2px 0;&quot;&gt;🔨&lt;/div&gt;
               &lt;div style=&quot;font-size: 9px; color: #555; line-height: 1.2;&quot;&gt;변수타입&lpar;Parent&rpar; 보고 &lt;strong&gt;결정됨&lt;/strong&gt;&lt;/div&gt;
            &lt;/div&gt;

            &lt;div style=&quot;flex: 1; border: 1px dashed #aaa; border-radius: 6px; padding: 6px; opacity: 0.5;&quot;&gt;
               &lt;div style=&quot;font-size: 9px; color: #777;&quot;&gt;Run Time&lt;/div&gt;
               &lt;div style=&quot;font-size: 18px; margin: 2px 0;&quot;&gt;🏃‍♂️&lt;/div&gt;
               &lt;div style=&quot;font-size: 9px; color: #777; line-height: 1.2;&quot;&gt;실제 객체&lpar;Child&rpar; 확인 안 함&lt;/div&gt;
            &lt;/div&gt;
          &lt;/div&gt;
          
          &lt;p style=&quot;margin: 0; font-size: 12px; color: #999; line-height: 1.4;&quot;&gt;
            컴파일 시점에 결정&lpar;Static Binding&rpar;되므로&lt;br /&gt;런타임의 오버라이딩 불가능
          &lt;/p&gt;
        &lt;/div&gt;
      &lt;/div&gt;

&lt;/div&gt;

&lt;div class=&quot;story-box&quot;&gt;

  &lt;h3 id=&quot;gc-&quot;&gt;1&rpar; 메모리 관리의 유연성 저하 &lpar;GC 미적용&rpar;&lt;/h3&gt;
  &lt;p&gt;인스턴스&lpar;객체&rpar;는 사용되지 않으면 &lt;strong&gt;Garbage Collector&lpar;GC&rpar;&lt;/strong&gt;가 메모리를 자동으로 정리합니다. 하지만 Static 메소드는 프로그램이 시작될 때 로드되어 &lt;strong class=&quot;highlight-text&quot;&gt;프로그램이 종료될 때까지 메모리에 계속 상주&lt;/strong&gt;합니다. 따라서 Static 멤버가 과도하게 많다면 시스템 메모리 효율을 오히려 떨어뜨릴 수 있습니다.&lt;/p&gt;

  &lt;h3 id=&quot;oop-&quot;&gt;2&rpar; 객체 지향 프로그래밍&lpar;OOP&rpar;의 제약&lt;/h3&gt;
  &lt;p&gt;Static 메소드는 &lt;strong class=&quot;highlight-text&quot;&gt;‘객체’가 아닌 ‘클래스’에 속하기 때문에&lt;/strong&gt;, 객체 지향의 핵심 기능들을 사용할 수 없습니다.&lt;/p&gt;
  &lt;ul&gt;
    &lt;li&gt;&lt;strong&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;this&lt;/code&gt; 사용 불가:&lt;/strong&gt; 객체가 생성되기 전에 존재하므로, 특정 객체의 상태&lpar;인스턴스 변수&rpar;에 접근할 수 없습니다.&lt;/li&gt;
    &lt;li&gt;&lt;strong&gt;오버라이딩 불가:&lt;/strong&gt; Static 메소드는 컴파일 시점에 호출 대상이 정해지므로&lpar;Static Binding&rpar;, 상속을 통한 다형성&lpar;오버라이딩&rpar;을 구현할 수 없습니다. 이는 코드의 확장성과 유연성을 떨어뜨리는 원인이 됩니다.&lt;/li&gt;
  &lt;/ul&gt;

&lt;/div&gt;</td></tr><tr><td width='20%'>DATE</td><td width='80%'><a href='https://shinhyeong.github.io/java/the-dangers-of-overusing-static-variables/'><b>[Java] Static 변수를 남용하면 안되는 이유 &lpar;단점&rpar;</b></a><br/>&lt;div class=&quot;story-box&quot;&gt;

  &lt;p&gt;개발을 하다 보면 객체 생성 없이 바로 접근할 수 있는 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;static&lt;/code&gt; 변수의 편리함에 끌릴 때가 있습니다. 하지만 이 편리함 뒤에는 &lt;strong class=&quot;highlight-text&quot;&gt;‘공유’&lt;/strong&gt;라는 치명적인 특성이 숨어 있습니다.&lt;/p&gt;

  &lt;p&gt;오늘은 Static 변수와 인스턴스 변수의 결정적인 차이를 알아보고, 왜 Static 변수를 상태 관리에 사용하면 안 되는지 구체적인 예시를 통해 알아보겠습니다.&lt;/p&gt;

&lt;/div&gt;

&lt;h2 id=&quot;static-변수-vs-instance-변수&quot;&gt;Static 변수 vs. Instance 변수&lt;/h2&gt;

&lt;div class=&quot;story-box&quot;&gt;

  &lt;p&gt;가장 먼저 이해해야 할 것은 &lt;strong class=&quot;highlight-text&quot;&gt;‘데이터가 어디에 저장되고, 누구와 공유되는가’&lt;/strong&gt;입니다. 이 차이가 모든 문제의 시작점입니다.&lt;/p&gt;

&lt;/div&gt;

&lt;div class=&quot;info-box&quot; style=&quot;max-width: 800px; margin: 0 auto 2rem auto; font-family: &#39;Pretendard&#39;, -apple-system, sans-serif; background-color: #f8f9fa; border-radius: 12px; padding: 30px; box-shadow: 0 4px 20px rgba&lpar;0,0,0,0.05&rpar;; color: #333;&quot;&gt;
  &lt;div style=&quot;display: flex; gap: 20px; flex-wrap: wrap;&quot;&gt;
    &lt;div style=&quot;flex: 1; min-width: 300px; background: #fff; border: 2px solid #e74c3c; border-radius: 12px; padding: 35px 20px 25px 20px; position: relative; overflow: hidden; box-shadow: 0 4px 15px rgba&lpar;231, 76, 60, 0.15&rpar;; display: flex; flex-direction: column; align-items: center;&quot;&gt;
      &lt;div style=&quot;position: absolute; top: 0; left: 0; background: #e74c3c; color: #fff; padding: 5px 15px; font-size: 12px; font-weight: bold; border-bottom-right-radius: 10px;&quot;&gt;위험 &lpar;공유&rpar;&lt;/div&gt;
      &lt;div style=&quot;text-align: center; color: #e74c3c; margin: 0 0 5px 0; font-size: 22px; font-weight: 800;&quot;&gt;Static 변수&lt;/div&gt;
      &lt;p style=&quot;text-align: center; font-size: 14px; color: #7f8c8d; margin: 0 0 20px 0; font-weight: 500;&quot;&gt;Method Area &lpar;클래스 로딩 시 1회 생성&rpar;&lt;/p&gt;
      &lt;div style=&quot;margin: 10px 0 20px 0;&quot;&gt;
        &lt;span style=&quot;font-size: 60px; filter: drop-shadow&lpar;0 4px 6px rgba&lpar;231, 76, 60, 0.3&rpar;&rpar;;&quot;&gt;☁️&lt;/span&gt;
      &lt;/div&gt;
      &lt;div style=&quot;font-weight: 800; color: #c0392b; margin-bottom: 15px; font-size: 15px;&quot;&gt;단 하나의 공유 공간&lt;/div&gt;
      &lt;div style=&quot;display: flex; justify-content: center; align-items: center; gap: 15px; width: 100%;&quot;&gt;
        &lt;div style=&quot;display: flex; flex-direction: column; gap: 8px;&quot;&gt;
          &lt;div style=&quot;background: #ecf0f1; padding: 6px 10px; border-radius: 15px; font-size: 11px; display: flex; align-items: center; gap: 4px; color: #555;&quot;&gt;&lt;span style=&quot;font-size: 14px;&quot;&gt;🤖&lt;/span&gt; 객체 A&lt;/div&gt;
          &lt;div style=&quot;background: #ecf0f1; padding: 6px 10px; border-radius: 15px; font-size: 11px; display: flex; align-items: center; gap: 4px; color: #555;&quot;&gt;&lt;span style=&quot;font-size: 14px;&quot;&gt;👾&lt;/span&gt; 객체 B&lt;/div&gt;
          &lt;div style=&quot;background: #ecf0f1; padding: 6px 10px; border-radius: 15px; font-size: 11px; display: flex; align-items: center; gap: 4px; color: #555;&quot;&gt;&lt;span style=&quot;font-size: 14px;&quot;&gt;🎃&lt;/span&gt; 객체 C&lt;/div&gt;
        &lt;/div&gt;
        &lt;div style=&quot;display: flex; flex-direction: column; justify-content: center; color: #e74c3c; font-size: 20px; font-weight: bold;&quot;&gt;
             &lt;span&gt;↘️&lt;/span&gt;&lt;span&gt;➡️&lt;/span&gt;&lt;span&gt;↗️&lt;/span&gt;
        &lt;/div&gt;
        &lt;div style=&quot;background: #fadbd8; border: 3px dotted #e74c3c; padding: 10px; border-radius: 12px; text-align: center; flex: 1; display: flex; flex-direction: column; align-items: center; justify-content: center; min-height: 80px;&quot;&gt;
          &lt;div style=&quot;font-size: 28px; margin-bottom: 5px;&quot;&gt;📦&lt;/div&gt;
          &lt;div style=&quot;font-weight: bold; color: #c0392b; font-size: 12px; line-height: 1.2;&quot;&gt;실제 값&lt;br /&gt;&lpar;모두가 여기를 봄&rpar;&lt;/div&gt;
        &lt;/div&gt;
      &lt;/div&gt;
    &lt;/div&gt;
    &lt;div style=&quot;flex: 1; min-width: 300px; background: #fff; border: 2px solid #27ae60; border-radius: 12px; padding: 35px 20px 25px 20px; position: relative; overflow: hidden; box-shadow: 0 4px 15px rgba&lpar;39, 174, 96, 0.15&rpar;; display: flex; flex-direction: column; align-items: center;&quot;&gt;
      &lt;div style=&quot;position: absolute; top: 0; left: 0; background: #27ae60; color: #fff; padding: 5px 15px; font-size: 12px; font-weight: bold; border-bottom-right-radius: 10px;&quot;&gt;안전 &lpar;독립&rpar;&lt;/div&gt;
      &lt;div style=&quot;text-align: center; color: #27ae60; margin: 0 0 5px 0; font-size: 22px; font-weight: 800;&quot;&gt;Instance 변수&lt;/div&gt;
      &lt;p style=&quot;text-align: center; font-size: 14px; color: #7f8c8d; margin: 0 0 20px 0; font-weight: 500;&quot;&gt;Heap Area &lpar;객체 생성 시 마다 생성&rpar;&lt;/p&gt;
      &lt;div style=&quot;margin: 10px 0 20px 0; display: flex; gap: 15px;&quot;&gt;
        &lt;span style=&quot;font-size: 50px; filter: drop-shadow&lpar;0 4px 6px rgba&lpar;39, 174, 96, 0.3&rpar;&rpar;;&quot;&gt;📦&lt;/span&gt;
        &lt;span style=&quot;font-size: 50px; filter: drop-shadow&lpar;0 4px 6px rgba&lpar;39, 174, 96, 0.3&rpar;&rpar;; opacity: 0.6;&quot;&gt;📦&lt;/span&gt;
      &lt;/div&gt;
      &lt;div style=&quot;font-weight: 800; color: #1e8449; margin-bottom: 15px; font-size: 15px;&quot;&gt;객체별 독립 공간&lt;/div&gt;
      &lt;div style=&quot;display: flex; flex-direction: column; gap: 12px; width: 100%; margin-top: 5px;&quot;&gt;
        &lt;div style=&quot;display: flex; align-items: center; gap: 10px;&quot;&gt;
          &lt;div style=&quot;background: #ecf0f1; padding: 8px 10px; border-radius: 15px; font-size: 11px; width: 70px; display: flex; align-items: center; justify-content: center; gap: 4px; color: #555;&quot;&gt;&lt;span style=&quot;font-size: 14px;&quot;&gt;🤖&lt;/span&gt; 객체 A&lt;/div&gt;
          &lt;div style=&quot;color: #27ae60; font-size: 20px; font-weight: bold;&quot;&gt;➡️&lt;/div&gt;
          &lt;div style=&quot;background: #d5f5e3; border: 2px solid #27ae60; padding: 8px 10px; border-radius: 12px; font-size: 12px; flex: 1; display: flex; align-items: center; gap: 8px; color: #1e8449; font-weight: bold;&quot;&gt;
            &lt;span style=&quot;font-size: 18px;&quot;&gt;👜&lt;/span&gt; A 주머니 속 값
          &lt;/div&gt;
        &lt;/div&gt;
        &lt;div style=&quot;display: flex; align-items: center; gap: 10px;&quot;&gt;
          &lt;div style=&quot;background: #ecf0f1; padding: 8px 10px; border-radius: 15px; font-size: 11px; width: 70px; display: flex; align-items: center; justify-content: center; gap: 4px; color: #555;&quot;&gt;&lt;span style=&quot;font-size: 14px;&quot;&gt;👾&lt;/span&gt; 객체 B&lt;/div&gt;
          &lt;div style=&quot;color: #27ae60; font-size: 20px; font-weight: bold;&quot;&gt;➡️&lt;/div&gt;
          &lt;div style=&quot;background: #d5f5e3; border: 2px solid #27ae60; padding: 8px 10px; border-radius: 12px; font-size: 12px; flex: 1; display: flex; align-items: center; gap: 8px; color: #1e8449; font-weight: bold;&quot;&gt;
            &lt;span style=&quot;font-size: 18px;&quot;&gt;🎒&lt;/span&gt; B 주머니 속 값
          &lt;/div&gt;
        &lt;/div&gt;
      &lt;/div&gt;
    &lt;/div&gt;
  &lt;/div&gt;
&lt;/div&gt;

&lt;div class=&quot;story-box&quot;&gt;

  &lt;ul&gt;
    &lt;li&gt;&lt;strong&gt;Static 변수 &lpar;공용 칠판&rpar;&lt;/strong&gt;
      &lt;ul&gt;
        &lt;li&gt;프로그램이 시작될 때 &lt;strong&gt;Method Area&lt;/strong&gt;에 딱 &lt;strong&gt;하나&lt;/strong&gt;만 생성됩니다.&lt;/li&gt;
        &lt;li&gt;모든 인스턴스&lpar;객체&rpar;가 이 &lt;strong class=&quot;highlight-text&quot;&gt;하나의 공간을 공유&lt;/strong&gt;합니다.&lt;/li&gt;
        &lt;li&gt;쉽게 말해, 교실 앞에 있는 &lt;strong&gt;‘공용 칠판’&lt;/strong&gt;과 같습니다. 누군가 칠판에 낙서를 하면, 반 전체 학생이 그 낙서를 보게 됩니다.&lt;/li&gt;
      &lt;/ul&gt;
    &lt;/li&gt;
    &lt;li&gt;&lt;strong&gt;Instance 변수 &lpar;개인 공책&rpar;&lt;/strong&gt;
      &lt;ul&gt;
        &lt;li&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;new&lt;/code&gt; 연산자로 객체를 생성할 때마다 &lt;strong&gt;Heap Area&lt;/strong&gt;에 &lt;strong class=&quot;highlight-text&quot;&gt;매번 새로&lt;/strong&gt; 생성됩니다.&lt;/li&gt;
        &lt;li&gt;각 객체는 자신만의 독립적인 값을 가집니다.&lt;/li&gt;
        &lt;li&gt;이는 학생 개개인이 가진 &lt;strong&gt;‘개인 공책’&lt;/strong&gt;과 같습니다. 내가 공책에 필기를 해도 짝꿍의 공책에는 아무런 영향을 주지 않습니다.&lt;/li&gt;
      &lt;/ul&gt;
    &lt;/li&gt;
  &lt;/ul&gt;

&lt;/div&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;h2 id=&quot;static-남용-시-발생하는-문제점&quot;&gt;Static 남용 시 발생하는 문제점&lt;/h2&gt;

&lt;div class=&quot;story-box&quot;&gt;

  &lt;p&gt;“공유한다”는 것은 효율적으로 보일 수 있지만, 값이 수시로 변하는 상황&lpar;&lt;strong class=&quot;highlight-text&quot;&gt;가변 상태&lt;/strong&gt;&rpar;에서는 재앙이 될 수 있습니다. 대표적인 두 가지 문제 상황을 시뮬레이션 해보겠습니다.&lt;/p&gt;

&lt;/div&gt;

&lt;div class=&quot;info-box&quot; style=&quot;max-width: 1200px; margin: 0 auto 2rem auto; font-family: &#39;Pretendard&#39;, -apple-system, sans-serif; display: flex; gap: 20px; flex-wrap: wrap; align-items: stretch;&quot;&gt;
    &lt;div style=&quot;flex: 1; min-width: 320px; background: #fff; border: 1px solid #e0e0e0; border-top: 5px solid #e67e22; border-radius: 8px; box-shadow: 0 4px 15px rgba&lpar;0,0,0,0.05&rpar;; overflow: hidden; display: flex; flex-direction: column;&quot;&gt;
        &lt;div style=&quot;padding: 15px 20px; border-bottom: 1px solid #f0f0f0; background: #fffcf5;&quot;&gt;
        &lt;div style=&quot;margin: 0; color: #d35400; font-size: 18px; display: flex; align-items: center; font-weight: 700;&quot;&gt;
            &lt;span style=&quot;font-size: 22px; margin-right: 8px;&quot;&gt;1️⃣&lt;/span&gt; 데이터 덮어쓰기 &lpar;Overwritting&rpar;
        &lt;/div&gt;
        &lt;p style=&quot;margin: 5px 0 0 0; font-size: 13px; color: #888;&quot;&gt;&quot;나는 철수를 저장했는데, 왜 영희가 나오지?&quot;&lt;/p&gt;
        &lt;/div&gt;
        &lt;div style=&quot;padding: 25px 15px; display: flex; flex-direction: column; gap: 20px; flex: 1; justify-content: center;&quot;&gt;
        &lt;div style=&quot;display: flex; align-items: center; justify-content: center; gap: 8px; flex-wrap: nowrap;&quot;&gt; &lt;div style=&quot;flex: 1; min-width: 90px; text-align: center; position: relative;&quot;&gt;
            &lt;div style=&quot;position: absolute; top: -10px; left: 50%; transform: translateX&lpar;-50%&rpar;; background: #e67e22; color: #fff; font-size: 9px; font-weight: bold; padding: 2px 6px; border-radius: 10px;&quot;&gt;STEP 1&lt;/div&gt;
            &lt;div style=&quot;font-size: 24px; margin-bottom: 4px;&quot;&gt;🤖&lt;/div&gt; &lt;div style=&quot;font-size: 11px; font-weight: bold; color: #555;&quot;&gt;객체 A&lt;/div&gt;
            &lt;div style=&quot;background: #fdf2e9; border: 1px solid #f5cba7; color: #d35400; font-size: 10px; padding: 4px; border-radius: 6px; margin-top: 4px; white-space: nowrap;&quot;&gt; name = &lt;strong&gt;철수&lt;/strong&gt; ➡️ 
            &lt;/div&gt;
            &lt;/div&gt;
            &lt;div style=&quot;flex: 1.2; min-width: 120px; background: #fff; border: 2px dashed #d35400; border-radius: 10px; padding: 12px 8px; text-align: center; position: relative; z-index: 1;&quot;&gt; &lt;div style=&quot;position: absolute; top: -8px; left: 50%; transform: translateX&lpar;-50%&rpar;; background: #fff; border: 1px solid #d35400; color: #d35400; font-size: 9px; font-weight: bold; padding: 1px 6px; border-radius: 4px; white-space: nowrap;&quot;&gt;공유된 Static 변수&lt;/div&gt;
            &lt;div style=&quot;margin-top: 8px; display: flex; flex-direction: column; align-items: center; gap: 3px;&quot;&gt;
                &lt;div style=&quot;color: #ccc; text-decoration: line-through; font-size: 12px;&quot;&gt;name = &quot;철수&quot;&lt;/div&gt;
                &lt;div style=&quot;color: #d35400; font-size: 14px;&quot;&gt;⬇️&lt;/div&gt;
                &lt;div style=&quot;color: #d35400; font-size: 14px; font-weight: 800; background: #fffcf5; padding: 3px 5px;border-radius: 4px;&quot;&gt;name = &quot;영희&quot;&lt;/div&gt;
            &lt;/div&gt;
            &lt;/div&gt;
            &lt;div style=&quot;flex: 1; min-width: 90px; text-align: center; position: relative;&quot;&gt;
            &lt;div style=&quot;position: absolute; top: -10px; left: 50%; transform: translateX&lpar;-50%&rpar;; background: #e67e22; color: #fff; font-size: 9px; font-weight: bold; padding: 2px 6px; border-radius: 10px; opacity: 0.8;&quot;&gt;STEP 2&lt;/div&gt;
            &lt;div style=&quot;font-size: 24px; margin-bottom: 4px;&quot;&gt;👾&lt;/div&gt; &lt;div style=&quot;font-size: 11px; font-weight: bold; color: #555;&quot;&gt;객체 B&lt;/div&gt;
            &lt;div style=&quot;background: #fdf2e9; border: 1px solid #f5cba7; color: #d35400; font-size: 10px; padding: 4px; border-radius: 6px; margin-top: 4px; white-space: nowrap;&quot;&gt;⬅️ name = &lt;strong&gt;영희&lt;/strong&gt;
            &lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        &lt;/div&gt;
        &lt;div style=&quot;background: #fbeee6; padding: 15px; text-align: center; border-top: 1px solid #f0e0d0; margin-top: auto;&quot;&gt;
        &lt;div style=&quot;display: inline-block; text-align: left;&quot;&gt;
            &lt;span style=&quot;font-size: 14px;&quot;&gt;🤯 &lt;strong&gt;결과:&lt;/strong&gt; 나중에 &lt;strong&gt;객체 A&lt;/strong&gt;가 확인하면?&lt;/span&gt;&lt;br /&gt;
            &lt;span style=&quot;font-size: 13px; color: #a04000; margin-left: 24px;&quot;&gt;→ &quot;철수&quot;는 사라지고 &lt;strong&gt;&quot;영희&quot;&lt;/strong&gt;만 남음.&lt;/span&gt;
        &lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;

    &lt;div style=&quot;flex: 1; min-width: 340px; background: #fff; border: 1px solid #e0e0e0; border-top: 5px solid #c0392b; border-radius: 8px; box-shadow: 0 4px 15px rgba&lpar;0,0,0,0.05&rpar;; overflow: hidden; display: flex; flex-direction: column;&quot;&gt;
        &lt;div style=&quot;padding: 15px 20px; border-bottom: 1px solid #f0f0f0; background: #fff5f5;&quot;&gt;
        &lt;div style=&quot;margin: 0; color: #c0392b; font-size: 18px; display: flex; align-items: center; font-weight: 700;&quot;&gt;
            &lt;span style=&quot;font-size: 22px; margin-right: 8px;&quot;&gt;2️⃣&lt;/span&gt; 동시성 문제 &lpar;Race Condition&rpar;
        &lt;/div&gt;
        &lt;p style=&quot;margin: 5px 0 0 0; font-size: 13px; color: #888;&quot;&gt;동시에 접근해서 계산이 누락되는 문제&lt;/p&gt;
        &lt;/div&gt;
        &lt;div style=&quot;padding: 30px 20px; background: #fff; position: relative; flex: 1;&quot;&gt;
        &lt;div style=&quot;position: absolute; left: 50%; top: 20px; bottom: 20px; width: 2px; background: #f0f0f0; transform: translateX&lpar;-1px&rpar;; z-index: 0;&quot;&gt;&lt;/div&gt;
        &lt;div style=&quot;position: absolute; left: 50%; bottom: 10px; transform: translateX&lpar;-50%&rpar;; font-size: 10px; color: #ccc; background: #fff; padding: 2px;&quot;&gt;시간 흐름 ▼&lt;/div&gt;
        &lt;div style=&quot;text-align: center; margin-bottom: 25px; position: relative; z-index: 1;&quot;&gt;
            &lt;div style=&quot;display: inline-block; background: #333; color: #fff; padding: 5px 15px; border-radius: 20px; font-size: 12px; font-weight: bold;&quot;&gt;
            공유 변수: 0
            &lt;/div&gt;
        &lt;/div&gt;
        &lt;div style=&quot;display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px; position: relative; z-index: 1;&quot;&gt;
            &lt;div style=&quot;flex: 1; text-align: right; padding-right: 10px;&quot;&gt;
            &lt;div style=&quot;font-size: 11px; font-weight: bold; color: #c0392b;&quot;&gt;⚡️ 스레드 A&lt;/div&gt;
            &lt;div style=&quot;display: inline-block; border: 1px solid #ccc; padding: 6px; border-radius: 8px; background: #fff; font-size: 11px; color: #555;&quot;&gt;
                &quot;현재 값 &lt;strong&gt;0&lt;/strong&gt; 읽음&quot;
            &lt;/div&gt;
            &lt;/div&gt;
            &lt;div style=&quot;background: #efefef; color: #555; font-size: 10px; font-weight: bold; padding: 3px 6px; border-radius: 10px; border: 1px solid #ccc; white-space: nowrap;&quot;&gt;STEP 1&lt;/div&gt;
            &lt;div style=&quot;flex: 1;&quot;&gt;&lt;/div&gt;
        &lt;/div&gt;
        &lt;div style=&quot;display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px; position: relative; z-index: 1;&quot;&gt;
            &lt;div style=&quot;flex: 1;&quot;&gt;&lt;/div&gt; 
            &lt;div style=&quot;background: #c0392b; color: #fff; font-size: 10px; font-weight: bold; padding: 3px 6px; border-radius: 10px; white-space: nowrap;&quot;&gt;STEP 2&lt;/div&gt;
            &lt;div style=&quot;flex: 1; text-align: left; padding-left: 10px;&quot;&gt;
            &lt;div style=&quot;font-size: 11px; font-weight: bold; color: #c0392b;&quot;&gt;⚡️ 스레드 B&lt;/div&gt;
            &lt;div style=&quot;display: inline-block; border: 2px solid #c0392b; padding: 6px; border-radius: 8px; background: #fff5f5; font-size: 11px; color: #c0392b;&quot;&gt;
                &quot;나도 &lt;strong&gt;0&lt;/strong&gt; 읽음!&quot;&lt;br /&gt;
                &lt;span style=&quot;font-size: 9px; background: #c0392b; color: #fff; padding: 1px 4px; border-radius: 2px;&quot;&gt;⚠️ A 저장 전!&lt;/span&gt;
            &lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        &lt;div style=&quot;display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px; position: relative; z-index: 1;&quot;&gt;
            &lt;div style=&quot;flex: 1; text-align: right; padding-right: 10px;&quot;&gt;
            &lt;div style=&quot;display: inline-block; border: 1px solid #ccc; padding: 6px; border-radius: 8px; background: #f9f9f9; font-size: 11px; color: #999;&quot;&gt;
                &quot;0+1 = &lt;strong&gt;1&lt;/strong&gt; 저장&quot;
            &lt;/div&gt;
            &lt;/div&gt;
            &lt;div style=&quot;background: #efefef; color: #555; font-size: 10px; font-weight: bold; padding: 3px 6px; border-radius: 10px; border: 1px solid #ccc; white-space: nowrap;&quot;&gt;STEP 3&lt;/div&gt;
            &lt;div style=&quot;flex: 1;&quot;&gt;&lt;/div&gt; 
        &lt;/div&gt;
        &lt;div style=&quot;display: flex; justify-content: space-between; align-items: center; position: relative; z-index: 1;&quot;&gt;
            &lt;div style=&quot;flex: 1;&quot;&gt;&lt;/div&gt; 
            &lt;div style=&quot;background: #efefef; color: #555; font-size: 10px; font-weight: bold; padding: 3px 6px; border-radius: 10px; border: 1px solid #ccc; white-space: nowrap;&quot;&gt;STEP 4&lt;/div&gt;
            &lt;div style=&quot;flex: 1; text-align: left; padding-left: 10px;&quot;&gt;
            &lt;div style=&quot;display: inline-block; border: 1px solid #ccc; padding: 6px; border-radius: 8px; background: #f9f9f9; font-size: 11px; color: #999;&quot;&gt;
                &quot;0+1 = &lt;strong&gt;1&lt;/strong&gt; 저장&quot; &lpar;덮어씀&rpar;
            &lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        &lt;/div&gt;
        &lt;div style=&quot;background: #fceaea; padding: 15px; text-align: center; border-top: 1px solid #f0e0d0; margin-top: auto;&quot;&gt;
        &lt;div style=&quot;display: inline-block; text-align: left;&quot;&gt;
            &lt;span style=&quot;font-size: 14px;&quot;&gt;🤯 &lt;strong&gt;결과:&lt;/strong&gt;&lt;/span&gt; 
            &lt;span style=&quot;font-size: 13px; color: #922b21; line-height: 1.5;&quot;&gt;
            A가 값을 바꾸기도 전&lpar;Step 3&rpar;에 &lt;br /&gt;B가 &lt;strong&gt;옛날 값&lpar;Step 2&rpar;을 읽어서&lt;/strong&gt; 둘 다 1을 저장함.
            &lt;/span&gt;
        &lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
&lt;/div&gt;

&lt;div class=&quot;story-box&quot;&gt;

  &lt;h3 id=&quot;section&quot;&gt;1&rpar; 객체 지향의 파괴 &lpar;캡슐화 위반&rpar;&lt;/h3&gt;

  &lt;p&gt;객체 지향 프로그래밍&lpar;OOP&rpar;의 핵심은 객체가 자신의 상태를 스스로 관리하고 보호하는 것입니다. 하지만 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;static&lt;/code&gt;으로 변수를 선언하면, 모든 객체가 하나의 변수를 공유하게 됩니다.&lt;/p&gt;

  &lt;p&gt;위의 예시처럼 &lt;strong&gt;객체 A&lt;/strong&gt;는 자신의 이름을 “철수”라고 저장했지만, &lt;strong&gt;객체 B&lt;/strong&gt;가 생성되면서 값을 “영희”로 바꾸면, &lt;strong&gt;객체 A&lt;/strong&gt;의 이름도 강제로 “영희”가 되어버립니다. 이는 객체 간의 독립성을 해치는 결과를 초래합니다.&lt;/p&gt;

  &lt;h3 id=&quot;race-condition&quot;&gt;2&rpar; 멀티스레드 환경에서의 Race Condition&lt;/h3&gt;

  &lt;p&gt;웹 애플리케이션&lpar;Spring 등&rpar;은 기본적으로 멀티스레드 환경입니다. 만약 사용자 정보를 저장하는 변수를 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;static&lt;/code&gt;으로 선언한다면 어떤 일이 벌어질까요?&lt;/p&gt;

  &lt;p&gt;사용자 A가 로그인하는 도중에 사용자 B가 접속하면, &lt;strong class=&quot;highlight-text&quot;&gt;사용자 A의 화면에 사용자 B의 정보가 노출&lt;/strong&gt;되는 사고가 발생할 수 있습니다. 스레드들이 공유 자원에 동시에 접근하면서 발생하는 이 &lt;strong&gt;경쟁 상태&lpar;Race Condition&rpar;&lt;/strong&gt;는 디버깅하기도 매우 어렵습니다.&lt;/p&gt;

&lt;/div&gt;

&lt;p&gt;&lt;br /&gt;&lt;/p&gt;

&lt;h2 id=&quot;그럼-언제-static을-써야-할까--올바른-사용법&quot;&gt;그럼 언제 Static을 써야 할까? &lt;span class=&quot;title-sub-desc&quot;&gt;: 올바른 사용법&lt;/span&gt;&lt;/h2&gt;

&lt;div class=&quot;story-box&quot;&gt;

  &lt;p&gt;&lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;static&lt;/code&gt;은 무조건 나쁜 것이 아닙니다. &lt;strong class=&quot;highlight-text&quot;&gt;“공유해도 안전한 데이터”&lt;/strong&gt;에 사용하면 메모리 효율을 높이고 코드를 간결하게 만들 수 있습니다.&lt;/p&gt;

&lt;/div&gt;

&lt;div class=&quot;info-box&quot; style=&quot;max-width: 800px; margin: 0 auto 2rem auto; font-family: &#39;Pretendard&#39;, -apple-system, sans-serif;&quot;&gt;
  &lt;div style=&quot;display: flex; gap: 20px; flex-wrap: wrap; align-items: stretch;&quot;&gt;
    &lt;div style=&quot;flex: 1; min-width: 300px; background: #fff; border: 1px solid #e0e0e0; border-top: 5px solid #2980b9; border-radius: 12px; box-shadow: 0 4px 15px rgba&lpar;41, 128, 185, 0.1&rpar;; overflow: hidden; display: flex; flex-direction: column;&quot;&gt;
      &lt;div style=&quot;padding: 20px; border-bottom: 1px solid #f0f0f0; background: #f4f9fd;&quot;&gt;
        &lt;div style=&quot;margin: 0; color: #2980b9; font-size: 18px; display: flex; align-items: center; font-weight: bold;&quot;&gt;
          &lt;span style=&quot;font-size: 22px; margin-right: 8px;&quot;&gt;💎&lt;/span&gt; 불변의 상수 &lpar;Constant&rpar;
        &lt;/div&gt;
        &lt;p style=&quot;margin: 5px 0 0 0; font-size: 13px; color: #666;&quot;&gt;변하지 않는 공통 값은 &lt;strong&gt;Static&lt;/strong&gt;으로!&lt;/p&gt;
      &lt;/div&gt;
      &lt;div style=&quot;padding: 25px; flex: 1; display: flex; flex-direction: column; align-items: center;&quot;&gt;
        &lt;div style=&quot;margin-bottom: 20px; text-align: center;&quot;&gt;
          &lt;div style=&quot;font-size: 40px; margin-bottom: 10px;&quot;&gt;🏫&lt;/div&gt;
          &lt;div style=&quot;font-size: 14px; font-weight: bold; color: #333;&quot;&gt;학교 이름 &lpar;School Name&rpar;&lt;/div&gt;
          &lt;div style=&quot;font-size: 12px; color: #888; margin-top: 5px;&quot;&gt;
            &quot;학생이 100명이든 1000명이든&lt;br /&gt;학교 이름은 하나로 똑같습니다.&quot;
          &lt;/div&gt;
        &lt;/div&gt;
        &lt;div style=&quot;background: #2c3e50; color: #ecf0f1; padding: 15px; border-radius: 8px; width: 100%; box-sizing: border-box; font-family: monospace; font-size: 12px; line-height: 1.5;&quot;&gt;
          &lt;span style=&quot;color: #e67e22;&quot;&gt;public static final&lt;/span&gt; String SCHOOL = &lt;span style=&quot;color: #f1c40f;&quot;&gt;&quot;JAVA HIGH&quot;&lt;/span&gt;;
        &lt;/div&gt;
        &lt;div style=&quot;margin-top: 15px; text-align: center;&quot;&gt;
          &lt;span style=&quot;background: #d6eaf8; color: #2980b9; padding: 4px 10px; border-radius: 12px; font-size: 11px; font-weight: bold;&quot;&gt;안전한 공유 &lpar;Read Only&rpar;&lt;/span&gt;
        &lt;/div&gt;
      &lt;/div&gt;
    &lt;/div&gt;
    &lt;div style=&quot;flex: 1; min-width: 300px; background: #fff; border: 1px solid #e0e0e0; border-top: 5px solid #27ae60; border-radius: 12px; box-shadow: 0 4px 15px rgba&lpar;39, 174, 96, 0.1&rpar;; overflow: hidden; display: flex; flex-direction: column;&quot;&gt;
      &lt;div style=&quot;padding: 20px; border-bottom: 1px solid #f0f0f0; background: #f0fdf4;&quot;&gt;
        &lt;div style=&quot;margin: 0; color: #27ae60; font-size: 18px; display: flex; align-items: center; font-weight: bold;&quot;&gt;
          &lt;span style=&quot;font-size: 22px; margin-right: 8px;&quot;&gt;👤&lt;/span&gt; 객체 고유 상태 &lpar;State&rpar;
        &lt;/div&gt;
        &lt;p style=&quot;margin: 5px 0 0 0; font-size: 13px; color: #666;&quot;&gt;개별적으로 다른 값은 &lt;strong&gt;Instance&lt;/strong&gt;로!&lt;/p&gt;
      &lt;/div&gt;
      &lt;div style=&quot;padding: 25px; flex: 1; display: flex; flex-direction: column; align-items: center;&quot;&gt;
        &lt;div style=&quot;margin-bottom: 20px; display: flex; gap: 20px;&quot;&gt;
          &lt;div style=&quot;text-align: center;&quot;&gt;
            &lt;div style=&quot;font-size: 30px;&quot;&gt;👦&lt;/div&gt;
            &lt;div style=&quot;background: #27ae60; color: #fff; font-size: 10px; padding: 2px 6px; border-radius: 4px; margin-top: 5px;&quot;&gt;철수&lt;/div&gt;
          &lt;/div&gt;
          &lt;div style=&quot;text-align: center;&quot;&gt;
            &lt;div style=&quot;font-size: 30px;&quot;&gt;👧&lt;/div&gt;
            &lt;div style=&quot;background: #27ae60; color: #fff; font-size: 10px; padding: 2px 6px; border-radius: 4px; margin-top: 5px;&quot;&gt;영희&lt;/div&gt;
          &lt;/div&gt;
        &lt;/div&gt;
        &lt;div style=&quot;font-size: 12px; color: #888; text-align: center; margin-bottom: 20px;&quot;&gt;
          &quot;학생마다 이름, 나이, 성적은&lt;br /&gt;모두 다릅니다.&quot;
        &lt;/div&gt;
        &lt;div style=&quot;background: #2c3e50; color: #ecf0f1; padding: 15px; border-radius: 8px; width: 100%; box-sizing: border-box; font-family: monospace; font-size: 12px; line-height: 1.5;&quot;&gt;
          &lt;span style=&quot;color: #e67e22;&quot;&gt;private&lt;/span&gt; String studentName;&lt;br /&gt;
          &lt;span style=&quot;color: #e67e22;&quot;&gt;private&lt;/span&gt; int grade;
        &lt;/div&gt;
        &lt;div style=&quot;margin-top: 15px; text-align: center;&quot;&gt;
          &lt;span style=&quot;background: #d5f5e3; color: #27ae60; padding: 4px 10px; border-radius: 12px; font-size: 11px; font-weight: bold;&quot;&gt;철저한 독립 &lpar;Capsulation&rpar;&lt;/span&gt;
        &lt;/div&gt;
      &lt;/div&gt;
    &lt;/div&gt;
  &lt;/div&gt;
&lt;/div&gt;

&lt;div class=&quot;story-box&quot;&gt;

  &lt;ul&gt;
    &lt;li&gt;&lt;strong&gt;상수&lpar;Constant&rpar;:&lt;/strong&gt; 모든 객체가 공통적으로 사용하며 값이 변하지 않는 데이터는 &lt;strong class=&quot;highlight-text&quot;&gt;static final&lt;/strong&gt;로 선언하여 메모리를 절약하고 안전하게 공유합니다. &lpar;예: &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Math.PI&lt;/code&gt;, &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Integer.MAX_VALUE&lt;/code&gt;&rpar;&lt;/li&gt;
    &lt;li&gt;&lt;strong&gt;유틸리티 메소드:&lt;/strong&gt; 객체의 상태&lpar;인스턴스 변수&rpar;를 사용하지 않고 입력받은 값으로만 처리하는 메소드는 &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;static&lt;/code&gt; 메소드로 만드는 것이 효율적입니다. &lpar;예: &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;Math.random&lpar;&rpar;&lt;/code&gt;, &lt;code class=&quot;language-plaintext highlighter-rouge&quot;&gt;StringUtils.isEmpty&lpar;&rpar;&lt;/code&gt;&rpar;&lt;/li&gt;
    &lt;li&gt;&lt;strong&gt;상태&lpar;State&rpar;:&lt;/strong&gt; 객체마다 달라져야 하는 데이터&lpar;이름, 나이, 잔고 등&rpar;는 반드시 &lt;strong class=&quot;highlight-text&quot;&gt;인스턴스 변수&lt;/strong&gt;로 선언하여 캡슐화를 지켜야 합니다.&lt;/li&gt;
  &lt;/ul&gt;

&lt;/div&gt;</td></tr><tr><td width='20%'>DATE</td><td width='80%'><a href='https://shinhyeong.github.io/java/why-main-method-is-static/'><b>Java의 main 메소드는 왜 static 메소드일까?</b></a><br/>&lt;h1 id=&quot;jvm객체를-생성하지-않고도-프로그램-시작할-수-있어야&quot;&gt;JVM←객체를 생성하지 않고도 프로그램 시작할 수 있어야&lt;/h1&gt;

&lt;hr /&gt;

&lt;h2 id=&quot;1-프로그램-실행-과정으로-이해해보자&quot;&gt;1. 프로그램 실행 과정으로 이해해보자&lt;/h2&gt;

&lt;ol&gt;
  &lt;li&gt;객체가 있어야 메소드 호출이 가능한데, 프로그램 시작 시점에는 &lt;em&gt;어떤 객체도 없는 상태&lt;/em&gt;.&lt;/li&gt;
  &lt;li&gt;JVM이 &lt;strong&gt;객체 생성 없이도 메서드를 호출&lt;/strong&gt;할 수 있어야 함&lt;/li&gt;
  &lt;li&gt;따라서 &lt;strong&gt;static&lt;/strong&gt;으로 선언하여 클래스 로딩 시점에 메모리에 로드되도록 함&lt;/li&gt;
&lt;/ol&gt;

&lt;hr /&gt;

&lt;h2 id=&quot;2-코드로-이해해보자&quot;&gt;2. 코드로 이해해보자&lt;/h2&gt;

&lt;h3 id=&quot;1-프로그램-시작-시점의-상황&quot;&gt;&lt;strong&gt;1&rpar; 프로그램 시작 시점의 상황&lt;/strong&gt;&lt;/h3&gt;

&lt;p&gt;어떤 객체도 생성되어 있지 않은 상태&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;MyProgram&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;static&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;main&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;[]&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;args&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
    
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;h3 id=&quot;2-만약-main이-static-메소드가-아니라면&quot;&gt;2&rpar; &lt;strong&gt;만약 main&lpar;&rpar;이 static 메소드가 아니라면,&lt;/strong&gt;&lt;/h3&gt;

&lt;p&gt;main 메소드를 호출하기 위해서는 &lt;strong&gt;MyProgram 객체가 필요함&lt;/strong&gt;&lt;/p&gt;

&lt;p&gt;그런데 &lt;strong&gt;누가 이 main 객체를 생성해야 하나?&lt;/strong&gt;&lt;/p&gt;

&lt;p&gt;JVM? 그러면 JVM이 생성자도 알아야 함&lt;/p&gt;

&lt;p&gt;또, 만약 생성자에 파라미터가 필요하다면?&lt;/p&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;MyProgram&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;main&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;[]&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;args&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
    
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;

&lt;h3 id=&quot;3-따라서-static-메소드로-선언한다&quot;&gt;&lt;strong&gt;3&rpar; 따라서 static 메소드로 선언한다&lt;/strong&gt;&lt;/h3&gt;

&lt;p&gt;main 메소드가 static 메소드가 되면&lt;/p&gt;

&lt;ol&gt;
  &lt;li&gt;&lt;strong&gt;객체 생성 없이 호출&lt;/strong&gt; 가능하고,&lt;/li&gt;
  &lt;li&gt;&lt;strong&gt;클래스 로딩 시점&lt;/strong&gt;에 메모리에 로드된다.&lt;/li&gt;
  &lt;li&gt;또, JVM이 &lt;strong&gt;바로 호출&lt;/strong&gt;할 수 있다.&lt;/li&gt;
&lt;/ol&gt;

&lt;div class=&quot;language-java highlighter-rouge&quot;&gt;&lt;div class=&quot;highlight&quot;&gt;&lt;pre class=&quot;highlight&quot;&gt;&lt;code&gt;&lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;class&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;MyProgram&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
    &lt;span class=&quot;kd&quot;&gt;public&lt;/span&gt; &lt;span class=&quot;kd&quot;&gt;static&lt;/span&gt; &lt;span class=&quot;kt&quot;&gt;void&lt;/span&gt; &lt;span class=&quot;nf&quot;&gt;main&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&lt;/span&gt;&lt;span class=&quot;nc&quot;&gt;String&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;[]&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;args&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&rpar;&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;{&lt;/span&gt;
        &lt;span class=&quot;c1&quot;&gt;// 이제 여기서부터 필요한 객체들을 생성할 수 있음&lt;/span&gt;
        &lt;span class=&quot;nc&quot;&gt;MyProgram&lt;/span&gt; &lt;span class=&quot;n&quot;&gt;program&lt;/span&gt; &lt;span class=&quot;o&quot;&gt;=&lt;/span&gt; &lt;span class=&quot;k&quot;&gt;new&lt;/span&gt; &lt;span class=&quot;nc&quot;&gt;MyProgram&lt;/span&gt;&lt;span class=&quot;o&quot;&gt;&lpar;&rpar;;&lt;/span&gt;
    &lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;span class=&quot;o&quot;&gt;}&lt;/span&gt;
&lt;/code&gt;&lt;/pre&gt;&lt;/div&gt;&lt;/div&gt;</td></tr><!-- BLOG-POST-LIST:END -->
  </table>
  
## Certification
- 📊 Advanced Data Analytics Semi-Professional(ADsP) [KOREA Data Agency] (2021.09.24)

## Awards and Honors
- 🥉 Naver PER BootCamp Personal Information Security Idea Contest - 3rd place [Naver] (2019.07.11)
- 🥉 2025 AWS Hackathon (GWNU X KNU) - 3rd place [AWS] (2025.11.23)
  - 🧪 [MVP Version Repo ↗](https://github.com/ShinHyeong/FactCheckAi) (Initial Prototype)
  - 🚀 [Final Version Repo ↗](https://github.com/saa-hackathon-2025/factcheck) (Final Submission)

## Skills

![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=ShinHyeong&langs_count=8&layout=compact&theme=buefy&hide_border=true)
