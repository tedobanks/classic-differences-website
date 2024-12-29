<template>
    <div class="privacy-policy">
        <div class="body">
            <!-- Title Section -->
            <div class="title-section">
                <h1>PRIVACY POLICY</h1>
                <p class="subtitle">Last updated December 29, 2024</p>
            </div>

            <!-- Introduction -->
            <div class="introduction">
                <p>
                    This Privacy Notice for CLASSIC DIFFERENCES LIMITED ('we',
                    'us', or 'our'), describes how and why we might access,
                    collect, store, use, and/or share ('process') your personal
                    information when you use our services ('Services'),
                    including when you:
                </p>
                <ul>
                    <li>
                        Visit our website at
                        <a
                            href="https://www.classicdifferences.com"
                            target="_blank"
                            >https://www.classicdifferences.com</a
                        >, or any website of ours that links to this Privacy
                        Notice
                    </li>
                    <li>
                        Engage with us in other related ways, including any
                        sales, marketing, or events
                    </li>
                </ul>
            </div>

            <!-- Table of Contents -->
            <div class="toc" id="toc">
                <h2>TABLE OF CONTENTS</h2>
                <ol>
                    <li
                        v-for="(section, index) in tableOfContents"
                        :key="index"
                    >
                        <a :href="'#' + section.id">{{ section.title }}</a>
                    </li>
                </ol>
            </div>

            <!-- Content Sections -->
            <div
                v-for="(section, index) in sections"
                :key="index"
                :id="section.id"
                class="content-section"
            >
                <h2>{{ section.title }}</h2>
                <div v-html="section.content"></div>
            </div>

            <!-- Contact Information -->
            <div id="contact" class="contact-section">
                <h2>HOW CAN YOU CONTACT US?</h2>
                <p>
                    If you have any questions about this Privacy Policy, you can
                    contact us:
                </p>
                <ul>
                    <li>By email: classicdifferenceslimited@gmail.com</li>
                    <li>By visiting our website: www.classicdifferences.com</li>
                    <li>
                        By mail: 1 Appleby court, Adenmore road, Catford,
                        London, SE6 4EJ, England
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from "vue";

const tableOfContents = ref([
    { id: "infocollect", title: "1. WHAT INFORMATION DO WE COLLECT?" },
    { id: "infouse", title: "2. HOW DO WE PROCESS YOUR INFORMATION?" },
    {
        id: "legalbases",
        title: "3. WHAT LEGAL BASES DO WE RELY ON TO PROCESS YOUR INFORMATION?",
    },
    {
        id: "whoshare",
        title: "4. WHEN AND WITH WHOM DO WE SHARE YOUR PERSONAL INFORMATION?",
    },
    {
        id: "cookies",
        title: "5. DO WE USE COOKIES AND OTHER TRACKING TECHNOLOGIES?",
    },
    { id: "inforetain", title: "6. HOW LONG DO WE KEEP YOUR INFORMATION?" },
    { id: "infosafe", title: "7. HOW DO WE KEEP YOUR INFORMATION SAFE?" },
    { id: "infominors", title: "8. DO WE COLLECT INFORMATION FROM MINORS?" },
    { id: "privacyrights", title: "9. WHAT ARE YOUR PRIVACY RIGHTS?" },
    { id: "DNT", title: "10. CONTROLS FOR DO-NOT-TRACK FEATURES" },
    {
        id: "uslaws",
        title: "11. DO UNITED STATES RESIDENTS HAVE SPECIFIC PRIVACY RIGHTS?",
    },
    { id: "policyupdates", title: "12. DO WE MAKE UPDATES TO THIS NOTICE?" },
    { id: "contact", title: "13. HOW CAN YOU CONTACT US ABOUT THIS NOTICE?" },
    {
        id: "request",
        title: "14. HOW CAN YOU REVIEW, UPDATE, OR DELETE THE DATA WE COLLECT FROM YOU?",
    },
]);

const sections = ref([
    {
        id: "infocollect",
        title: "1. WHAT INFORMATION DO WE COLLECT?",
        content: `
        <p>We collect personal information that you voluntarily provide to us when you express an interest in obtaining information about us or our products and Services.</p>
        <p><strong>Personal Information Provided by You:</strong> The personal information we collect depends on the context of your interactions with us and the Services, the choices you make, and the products and features you use. The personal information we collect may include:</p>
        <ul>
          <li>Email addresses</li>
          <li>Names</li>
        </ul>
      `,
    },
    {
        id: "infouse",
        title: "2. HOW DO WE PROCESS YOUR INFORMATION?",
        content: `
        <p><em><strong>In Short:</strong> We process your information to provide, improve, and administer our Services, communicate with you, for security and fraud prevention, and to comply with law.</em></p>
        <p>We process your personal information for a variety of reasons, depending on how you interact with our Services, including:</p>
        <ul>
          <li>To deliver and facilitate delivery of services to the user</li>
          <li>To respond to user inquiries/offer support to users</li>
          <li>To send administrative information to you</li>
          <li>To send marketing and promotional communications</li>
          <li>To save or protect an individual's vital interest</li>
        </ul>
      `,
    },
    {
        id: "legalbases",
        title: "3. WHAT LEGAL BASES DO WE RELY ON TO PROCESS YOUR INFORMATION?",
        content: `
        <p><em><strong>In Short:</strong> We only process your personal information when we believe it is necessary and we have a valid legal reason to do so under applicable law.</em></p>
        <p>The General Data Protection Regulation (GDPR) and UK GDPR require us to explain the valid legal bases we rely on to process your personal information. As such, we may rely on the following legal bases to process your personal information:</p>
        <ul>
          <li><strong>Consent</strong> - We may process your information if you have given us permission to use your personal information for a specific purpose.</li>
          <li><strong>Performance of a Contract</strong> - We may process your personal information when we believe it is necessary to fulfill our contractual obligations to you.</li>
          <li><strong>Legitimate Interests</strong> - We may process your information when we believe it is reasonably necessary to achieve our legitimate business interests.</li>
          <li><strong>Legal Obligations</strong> - We may process your information where we believe it is necessary for compliance with our legal obligations.</li>
        </ul>
      `,
    },
    {
        id: "whoshare",
        title: "4. WHEN AND WITH WHOM DO WE SHARE YOUR PERSONAL INFORMATION?",
        content: `
        <p><em><strong>In Short:</strong> We may share information in specific situations and with specific third parties.</em></p>
        <p>We may share or transfer your information in the following situations:</p>
        <ul>
          <li><strong>Business Transfers:</strong> We may share or transfer your information in connection with, or during negotiations of, any merger, sale of company assets, financing, or acquisition.</li>
          <li><strong>Business Partners:</strong> We may share your information with our business partners to offer you certain products, services, or promotions.</li>
          <li><strong>When we use Google Maps Platform APIs:</strong> We may share your information with certain Google Maps Platform APIs.</li>
        </ul>
      `,
    },
    {
        id: "cookies",
        title: "5. DO WE USE COOKIES AND OTHER TRACKING TECHNOLOGIES?",
        content: `
        <p><em><strong>In Short:</strong> We may use cookies and other tracking technologies to collect and store your information.</em></p>
        <p>We may use cookies and similar tracking technologies to access or store information. These technologies help us maintain the security of our Services, fix bugs, save your preferences, and assist with basic site functions.</p>
      `,
    },
    {
        id: "inforetain",
        title: "6. HOW LONG DO WE KEEP YOUR INFORMATION?",
        content: `
        <p><em><strong>In Short:</strong> We keep your information for as long as necessary to fulfill the purposes outlined in this Privacy Notice unless otherwise required by law.</em></p>
        <p>We will only keep your personal information for as long as it is necessary for the purposes set out in this Privacy Notice, unless a longer retention period is required or permitted by law.</p>
      `,
    },
    {
        id: "infosafe",
        title: "7. HOW DO WE KEEP YOUR INFORMATION SAFE?",
        content: `
        <p><em><strong>In Short:</strong> We aim to protect your personal information through a system of organizational and technical security measures.</em></p>
        <p>We have implemented appropriate technical and organizational security measures designed to protect the security of any personal information we process. However, despite our safeguards and efforts to secure your information, no electronic transmission over the Internet or information storage technology can be guaranteed to be 100% secure.</p>
      `,
    },
    {
        id: "infominors",
        title: "8. DO WE COLLECT INFORMATION FROM MINORS?",
        content: `
        <p><em><strong>In Short:</strong> We do not knowingly collect data from or market to children under 18 years of age.</em></p>
        <p>We do not knowingly solicit data from or market to children under 18 years of age. By using the Services, you represent that you are at least 18 or that you are the parent or guardian of such a minor and consent to such minor dependent's use of the Services.</p>
      `,
    },
    {
        id: "privacyrights",
        title: "9. WHAT ARE YOUR PRIVACY RIGHTS?",
        content: `
        <p><em><strong>In Short:</strong> You have rights that allow you greater access to and control over your personal information.</em></p>
        <p>Depending on your location, you may have certain rights regarding your personal information, including:</p>
        <ul>
          <li>Right to access your personal data</li>
          <li>Right to request correction of your personal data</li>
          <li>Right to request deletion of your personal data</li>
          <li>Right to withdraw consent</li>
          <li>Right to opt out of marketing communications</li>
        </ul>
      `,
    },
    {
        id: "DNT",
        title: "10. CONTROLS FOR DO-NOT-TRACK FEATURES",
        content: `
        <p>Most web browsers and some mobile operating systems include a Do-Not-Track ("DNT") feature or setting. However, there is no industry standard for how DNT requests should be handled; therefore, we do not currently respond to DNT signals.</p>
      `,
    },
    {
        id: "uslaws",
        title: "11. DO UNITED STATES RESIDENTS HAVE SPECIFIC PRIVACY RIGHTS?",
        content: `
        <p><em><strong>In Short:</strong> If you are a resident of certain US states, you have specific privacy rights.</em></p>
        <p>Depending on your state of residence, you may have certain additional rights regarding your personal information, including the right to:</p>
        <ul>
          <li>Request access to your personal information</li>
          <li>Request correction of your personal information</li>
          <li>Request deletion of your personal information</li>
          <li>Request portability of your personal information</li>
          <li>Opt out of certain data sharing practices</li>
        </ul>
      `,
    },
    {
        id: "policyupdates",
        title: "12. DO WE MAKE UPDATES TO THIS NOTICE?",
        content: `
        <p><em><strong>In Short:</strong> Yes, we will update this notice as necessary to stay compliant with relevant laws.</em></p>
        <p>We may update this Privacy Notice from time to time. The updated version will be indicated by an updated 'Revised' date at the top of this Privacy Notice.</p>
      `,
    },
    {
        id: "contact",
        title: "13. HOW CAN YOU CONTACT US ABOUT THIS NOTICE?",
        content: `
        <p>If you have questions about this notice, you can contact us:</p>
        <ul>
          <li>By email: classicdifferenceslimited@gmail.com</li>
          <li>By mail: 1 Appleby court, Adenmore road, Catford, London, SE6 4EJ, England</li>
          <li>By visiting our website: www.classicdifferences.com</li>
        </ul>
      `,
    },
    {
        id: "request",
        title: "14. HOW CAN YOU REVIEW, UPDATE, OR DELETE THE DATA WE COLLECT FROM YOU?",
        content: `
        <p>Based on the applicable laws of your country, you may have the right to request access to the personal information we collect from you, change that information, or delete it. To request to review, update, or delete your personal information, please submit a request form through our website.</p>
      `,
    },
]);
</script>

<style scoped>
.privacy-policy {
    font-family: Arial, sans-serif;
    max-width: 80%;
    margin: 0 auto;
    padding: 20px;
    color: #595959;
}

h1,
h2 {
    color: #000000;
}

h1 {
    font-size: 26px;
}

h2 {
    font-size: 19px;
    margin-top: 2em;
}

.subtitle {
    font-size: 14px;
    color: #595959;
}

a {
    color: #3030f1;
    text-decoration: none;
    word-break: break-word;
}

.content-section {
    margin-bottom: 2em;
}

ul {
    list-style-type: square;
    padding-left: 20px;
}

ul > li > ul {
    list-style-type: circle;
}

ul > li > ul > li > ul {
    list-style-type: square;
}

ol li {
    font-family: Arial;
}

.toc {
    margin: 2em 0;
}

.toc ol {
    padding-left: 20px;
}

.toc a {
    text-decoration: none;
    color: #3030f1;
}

.contact-section {
    margin-top: 3em;
    margin-bottom: 27%;
}


</style>
