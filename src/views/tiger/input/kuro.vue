<template>
  <div>
     <span class="input input--kuro">
					<input class="input__field input__field--kuro" type="text" id="input-7" />
					<label class="input__label input__label--kuro" for="input-7">
						<span class="input__label-content input__label-content--kuro">Verse</span>
					</label>
			</span>
  </div>  
</template>

<style scoped>
/* input */
		.input {
			position: relative;
			z-index: 1;
			display: inline-block;
			margin: 1em;
			max-width: 400px;
			width: calc(100% - 2em);
			vertical-align: top;
		}

		.input__field {
			position: relative;
			display: block;
			float: right;
			padding: 0.8em;
			width: 60%;
			border: none;
			border-radius: 0;
			background: #f0f0f0;
			color: #aaa;
			font-weight: bold;
			font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
			-webkit-appearance: none; /* for box shadows to show on iOS */
		}

		.input__field:focus {
			outline: none;
		}

		.input__label {
			display: inline-block;
			float: right;
			padding: 0 1em;
			width: 40%;
			color: #6a7989;
			font-weight: bold;
			font-size: 70.25%;
			-webkit-touch-callout: none;
			-webkit-user-select: none;
			-khtml-user-select: none;
			-moz-user-select: none;
			-ms-user-select: none;
			user-select: none;
		}

		.input__label-content {
			position: relative;
			display: block;
			padding: 1.6em 0;
			width: 100%;
		}

		.graphic {
			position: absolute;
			top: 0;
			left: 0;
			fill: none;
		}

		.icon {
			color: #ddd;
			font-size: 150%;
		}
        /* Kuro */
        .input--kuro {
            max-width: 320px;
            margin-bottom: 3em;
        }

        .input__field--kuro {
            width: 100%;
            background: transparent;
            color: #9196A1;
            opacity: 0;
            text-align: center;
            -webkit-transition: opacity 0.3s;
            transition: opacity 0.3s;
        }

        .input__label--kuro {
            position: absolute;
            left: 0;
            width: 100%;
            color: #df6589;
            pointer-events: none;
        }

        .input__label--kuro::before,
        .input__label--kuro::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 50%;
            height: 100%;
            border: 4px solid #747981;
            -webkit-transition: -webkit-transform 0.3s;
            transition: transform 0.3s;
        }

        .input__label--kuro::before {
            border-right: none;
        }

        .input__label--kuro::after {
            left: 50%;
            border-left: none;
        }

        .input__field--kuro:focus,
        .input--filled .input__field--kuro {
            opacity: 1;
            -webkit-transition-delay: 0.3s;
            transition-delay: 0.3s;
        }

        .input__field--kuro:focus + .input__label--kuro::before,
        .input--filled .input__label--kuro::before {
            -webkit-transform: translate3d(-10%, 0, 0);
            transform: translate3d(-10%, 0, 0);
        }

        .input__field--kuro:focus + .input__label--kuro::after,
        .input--filled .input__label--kuro::after {
            -webkit-transform: translate3d(10%, 0, 0);
            transform: translate3d(10%, 0, 0);
        }

        .input__field--kuro:focus + .input__label--kuro .input__label-content--kuro,
        .input--filled .input__label-content--kuro {
            -webkit-animation: anim-2 0.3s forwards;
            animation: anim-2 0.3s forwards;
        }

        @-webkit-keyframes anim-2 {
            50% {
                opacity: 0;
                -webkit-transform: scale3d(0.3, 0.3, 1);
                transform: scale3d(0.3, 0.3, 1);
            }
            51% {
                opacity: 0;
                -webkit-transform: translate3d(0, 3.7em, 0) scale3d(0.3, 0.3, 1);
                transform: translate3d(0, 3.7em, 0) scale3d(0.3, 0.3, 1);
            }
            100% {
                opacity: 1;
                -webkit-transform: translate3d(0, 3.7em, 0);
                transform: translate3d(0, 3.7em, 0);
            }
        }

        @keyframes anim-2 {
            50% {
                opacity: 0;
                -webkit-transform: scale3d(0.3, 0.3, 1);
                transform: scale3d(0.3, 0.3, 1);
            }
            51% {
                opacity: 0;
                -webkit-transform: translate3d(0, 3.7em, 0) scale3d(0.3, 0.3, 1);
                transform: translate3d(0, 3.7em, 0) scale3d(0.3, 0.3, 1);
            }
            100% {
                opacity: 1;
                -webkit-transform: translate3d(0, 3.7em, 0);
                transform: translate3d(0, 3.7em, 0);
            }
        }
</style>


