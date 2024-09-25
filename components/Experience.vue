<template>
    <section class="container my-5" id="experience">
        <h2>Experience</h2>
        <div class="card mb-3" v-for="(exp, index) in experiences" :key="index">
            <div class="card-body">
                <h5 class="card-title">{{ exp.company }}</h5>
                <span class="badge badge-primary">{{ exp.role }}</span>
                <p class="text-muted">{{ exp.duration }}</p>
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
                    duration: 'Juli 2021 - Saar ini',
                    jobdesk: [
                        'Mengkonfigurasi plugin website agar sesuai',
                        'Mengkonfigurasi tema agar website memiliki tampilan yang baik',
                        'Menerbitkan postingan ke website'
                    ]
                },
                {
                    company: 'PUSMENDIK',
                    role: 'Technical Team',
                    duration: 'Juli 2022 - Desember 2022',
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
                    duration: 'Januari 2023 - April 2023',
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