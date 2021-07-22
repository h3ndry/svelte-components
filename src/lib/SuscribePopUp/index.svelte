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
			<input type="checkbox" id="terms" name="terms" />
			<label for="terms">I agree to receive this newsletter and subscribe at any time.</label>
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

    h3 {
    	font-size: 2rem;
	line-height: 1.6;
	margin-bottom: .5rem;
	}

    .form {
        width: 80%;
        padding: 2rem 0 4rem 0;
        display: grid;
        grid-gap: 2rem;
    }
    .form .email-input {
    /* cheat... need to proper fix this */ 
        width: 90%;

        padding: 1.25rem;
        border-radius: 5px;
        border: solid 1px #A7AAC9;
    }

    .form-group #terms {
	-webkit-appearance: none;
	background-color: #fafafa;
	border: 1px solid #cacece;
	box-shadow: 0 1px 2px rgba(0,0,0,0.05), inset 0px -15px 10px -12px rgba(0,0,0,0.05);
	padding: 12px;
	border-radius: 3px;
	display: inline-block;
	position: relative;
	}
	
    .form-group #terms:checked:active {
	box-shadow: 0 1px 2px rgba(0,0,0,0.05), inset 0px 1px 3px rgba(0,0,0,0.1);
	}


    .form-group #terms:checked {
	background-color: #2D2865;
	border: 1px solid #adb8c0;
	box-shadow: 0 1px 2px rgba(0,0,0,0.05), inset 0px -15px 10px -12px rgba(0,0,0,0.05), inset 15px 10px -12px rgba(255,255,255,0.1);
	color: #99a1a7;
	}


    .form-group #terms:checked:after {
	content: '\2714';
	font-size: 14px;
	position: absolute;
	top: 0px;
	left: 3px;
	color: #99a1a7;
    }

    .btn-submit {
        background: #2D2865;
        border-radius: 5px;
        padding: 1.25rem;
        border: none;
	color: white;
    }

</style>
