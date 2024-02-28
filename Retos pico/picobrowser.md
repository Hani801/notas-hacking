## Objetivo
This website can be rendered only by **picobrowser**, go and catch the flag! `https://jupiter.challenges.picoctf.org/problem/26704/` ([link](https://jupiter.challenges.picoctf.org/problem/26704/)) or http://jupiter.challenges.picoctf.org:26704
## Solución
haniara-picoctf@webshell:~$ curl https://jupiter.challenges.picoctf.org/problem/26704/flag -H "User-Agent:picobrowser" grep | pico
<div class="jumbotron"> <p class="lead"></p> <p
            style="text-align:center; font-size:30px;"><b>Flag</b>:
            <code>picoCTF{p1c0_s3cr3t_ag3nt_e9b160d0}</code></p> <!--
            <p><a class="btn btn-lg btn-success" href="admin"
            role="button">Click here for the flag!</a> --> <!-- </p>
            -->
        </div> <footer class="footer"> <p>&copy; PicoCTF 2019</p>
        </footer>
    </div> <script> $(document).ready(function(){


        $(".close").click(function(){
            $("myAlert").alert("close");
        });
    });
    </script> </body>
</html>curl: (6) Could not resolve host: grep
## Notas

