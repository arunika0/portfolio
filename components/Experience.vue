<template>
    <section class="container my-5">
        <h2>Experience</h2>
        <div class="card mb-3" v-for="(exp, index) in experiences" :key="index">
            <div class="card-body">
                <h5 class="card-title">{{ exp.company }}</h5>
                <span class="badge badge-primary">{{ exp.role }}</span>
                <ul>
                    <li v-for="(job, jobIndex) in exp.jobdesk" :key="jobIndex">{{ job }}</li>
                </ul>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            experiences: [
                {
                    company: 'PSP FPIK UB',
                    role: 'Website Administrator',
                    jobdesk: [
                        'Mengkonfigurasi plugin website agar sesuai',
                        'Mengkonfigurasi tema agar website memiliki tampilan yang baik',
                        'Menerbitkan postingan ke website'
                    ]
                },
                {
                    company: 'PUSMENDIK',
                    role: 'Technical Team',
                    jobdesk: [
                        'Menjalankan query ke database untuk mengambil data',
                        'Mengkonfigurasi promotheus dan Grafana untuk memonitoring server',
                        'Mengkonfigurasi Postgresql agar dapat melakukan restore database',
                        'Digitalisasi Soal Asesmen Nasional',
                        'Menguji aplikasi apakah berfungsi semestinya',
                        'Backup dan Restore server PTN'
                    ]
                },
                {
                    company: 'WISECON',
                    role: 'DCT Support',
                    jobdesk: [
                        'Melakukan support kepada user yang terkendala melalui Helpdesk',
                        'Menjalankan query ke database untuk mengambil data',
                        'Membuat Manual Guide untuk user',
                        'Melakukan testing terhadap aplikasi atau software sebelum dipublikasi ke user'
                    ]
                }
            ],
        };
    },
};
</script>