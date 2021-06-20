<script lang="ts" charset="utf-8">
</script>

<div class="container">
    <button class="btn-close">x</button>
	<h3>Enjoyed the read?</h3>
	<p>Join our monthly newsletter for helpful tips on design and more.</p>

	<form action="" method="get" class="form">
		<div class="form-group">
			<label hidden for="email">Enter your email: </label>
			<input class='email-input' placeholder="Your email address" type="email" name="email" id="email" required />
		</div>
		<div class="form-group">
			<input type="checkbox" id="scales" name="scales" checked />
			<label for="scales">I agree to receive this newsletter and subscribe at any time.</label>
		</div>
            <button class="btn-submit" type="submit" >Subscribe</button>
	</form>
</div>

<style>

    .container {
        margin: 0 auto;
        width: 30rem;
        padding: 2rem;
        background-color: rgba(255, 255, 255, .73);
        display: grid;
        justify-items: center;
        border-radius: 1rem;
    }
    .btn-close {
        background-color: white;
        border: none;
        display: block;
        font-size: 1.5rem;
        /* padding: .5rem; */
        width: 2.5rem;
        height: 2.5rem;
        line-height: 0;
        border-radius: 50%;
        justify-self: end;
        align-self: center;
    }

    h3, p {
        color: #151936;
        text-align: center;
        width: 70%;
        margin: 0;
    }
    .form {
        width: 80%;
        padding: 2rem 0 4rem 0;
        display: grid;
        grid-gap: 1rem;
    }
    .form .email-input {
        width: 100%;
        padding: 0.862rem;
        border-radius: 5px;
        border: solid 1px #A7AAC9;
    }
    .btn-submit {
        background: #2D2865;
        border-radius: 5px;
        padding: 0.862rem;
        border: none;
    }

</style>
