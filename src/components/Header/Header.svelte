<script>

</script>

<main>
    <img src="/catlogo.svg" alt="the logo of the website" />
    <!-- <h1 class="logo"> PetSitters</h1> -->
	<div class="menu">
        <a href="#home">Home</a>
        <a href="#home">Servicios</a>
        <a href="#home">Training</a>
        <a href="#home">Blog</a>
        <a href="#home">Contacto</a>
    </div>
    <div class="login_menu">
        <a href="#home">Login</a>
        <a class="signup" href="#home">Sign Up</a>
    </div>
</main>

<style>
main{
    height:10vh;
    padding:6px 13vw;
    display:grid;
    align-items: center;
    grid-template-columns: .5fr 1fr 1fr;
    box-sizing: content-box;
}
main img{
    max-width: 6vw;
}
main > .menu,.login_menu {
    display:grid;
    grid-auto-flow: column;
    justify-self: right;
    grid-column-gap: 2rem;
}
main a {
    text-decoration: none;
    font-weight: 600;
    width:fit-content;
}
.menu a {
    color:white;
}
.menu a:hover {
    color:#ffc727;
}
.login_menu{
    display:grid;
    align-items: center;
    grid-column-gap: 1rem;
}
.login_menu a{
    color:#ffc727;
    font-weight: 600;
}
.signup{
    padding:6px 18px;
    border-radius: 12px;
    background-color: #ffc727;
    color:#333 !important;
    font-size: .8rem;
}
</style>