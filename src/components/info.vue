<template>
    <div>
        <p>{{ compEmail }} - {{ email }}</p>
        <p v-if='on_job'>Estou trabalhando no momento.</p>
        <p v-else>Estou em busca de novas oportunidades!</p>
        <p>Utilizo as seguintes tecnologias para back-end:</p>
        <ul>
            <li v-for='(stack, index) in backend_stack' v-bind:key='index'>
                {{ stack }}
                </li>
        </ul>
        <p>Ultilizo as seguintes tecnologias para font-end:</p>
        <ul>
            <li v-for='stack in frontend_stack' :key='stack.id'> 
                {{ stack.language }}
            </li>
        </ul>
        <div>
            <button @click='showEmail'>{{ textBtn }}</button>
        </div>
        <p v-show='show_email' class="transition">Mande uma mensagem para {{ email }}</p>
        <p>Para acessar o meu portfólio <a v-bind:href='meu_link' target='_blank'>basta clicar aqui</a></p>
        <pictureA style='width: 300px;'/>
    </div>
</template>

<script>
    import pictureA from './picture.vue';
    export default {
        name: 'info',
        components: {
            pictureA
        },
        props: {
            email: String,
            on_job: Boolean
        },
        data() {
            return {
                // on_job: true,
                show_email: false,
                // email: 'teste@teste.com',
                meu_link: 'https://google.com.br',
                textBtn: 'mostrar e-mail',
                backend_stack: ['Java', 'Python', 'NodeJs'],
                frontend_stack: [
                    {id: 1, language: 'HTML5'},
                    {id: 2, language: 'CSS3'},
                    {id: 3, language: 'Sass'}
                ]
            }
        },
        methods: {
            showEmail() {
               this.show_email = !this.show_email
               if(!this.show_email){
                   this.textBtn = 'mostrar e-mail'
               }else {
                   this.textBtn = 'esconder e-mail'
               }
            }
        }
    }
    
</script>

