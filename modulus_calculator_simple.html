<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>Modular calculator (x^y mod n, a x b mod n)</title>
    </head>
    <body style="font-family: Arial, Helvetica, sans-serif; font-size: 16px;">

        <b style="font-size:26px"><u>Power: x^y mod n</u></b><br />
        <span style="color:#555555">Use it to encrypt (C = M^e mod n) and decrypt (M = C^d mod n).</span>
        <br /><br />
        x (M or C): <input id="px" type="text" style="width:220px" value="11">
        &nbsp; y (e or d): <input id="py" type="text" style="width:220px" value="23">
        &nbsp; n: <input id="pn" type="text" style="width:220px" value="187">
        <br /><br />
        <button type="button" id="b1">Compute x^y mod n</button>
        <br /><br />
        Result: <input id="pans" type="text" style="width:500px; font-weight:bold" readonly="readonly">
        <br /><br /><br />

        <b style="font-size:26px"><u>Product: a x b mod n</u></b><br />
        <span style="color:#555555">Use it to check a key pair: (d x e) mod phi(n) must equal 1.</span>
        <br /><br />
        a: <input id="ma" type="text" style="width:220px" value="7">
        &nbsp; b: <input id="mb" type="text" style="width:220px" value="23">
        &nbsp; n: <input id="mn" type="text" style="width:220px" value="160">
        <br /><br />
        <button type="button" id="b2">Compute a x b mod n</button>
        <br /><br />
        Result: <input id="mans" type="text" style="width:500px; font-weight:bold" readonly="readonly">

        <script>
            // Whole numbers only: removes spaces and commas, rejects anything else.
            function cleanNumber(s) {
                s = String(s).replace(/[\s,]/g, "");
                if (s === "" || !/^[0-9]+$/.test(s)) { return null; }
                return s;
            }

            // Exact arithmetic with BigInt when the browser has it.
            var HAS_BIGINT = (typeof BigInt === "function");

            function powModBig(xs, ys, ns) {
                var x = BigInt(xs), y = BigInt(ys), n = BigInt(ns);
                var zero = BigInt(0), one = BigInt(1), two = BigInt(2);
                if (n === one) { return "0"; }
                var r = one;
                x = x % n;
                while (y > zero) {
                    if (y % two === one) { r = (r * x) % n; }
                    x = (x * x) % n;
                    y = y / two;
                }
                return r.toString();
            }

            // Fallback without BigInt: exact while n is below 94,906,265.
            var SAFE_N = 94906265;
            function powModSmall(x, y, n) {
                if (n === 1) { return 0; }
                var r = 1;
                x = x % n;
                while (y > 0) {
                    if (y % 2 === 1) { r = (r * x) % n; }
                    x = (x * x) % n;
                    y = Math.floor(y / 2);
                }
                return r;
            }

            document.getElementById("b1").onclick = function () {
                var x = cleanNumber(document.getElementById("px").value);
                var y = cleanNumber(document.getElementById("py").value);
                var n = cleanNumber(document.getElementById("pn").value);
                var out = document.getElementById("pans");
                if (x === null || y === null || n === null) { out.value = "Please enter whole numbers only."; return; }
                if (/^0+$/.test(n)) { out.value = "n must be greater than 0."; return; }
                if (HAS_BIGINT) {
                    out.value = powModBig(x, y, n);
                } else if (Number(n) < SAFE_N && Number(y) <= 9007199254740991) {
                    out.value = String(powModSmall(Number(x), Number(y), Number(n)));
                } else {
                    out.value = "Numbers too large for this browser.";
                }
            };

            document.getElementById("b2").onclick = function () {
                var a = cleanNumber(document.getElementById("ma").value);
                var b = cleanNumber(document.getElementById("mb").value);
                var n = cleanNumber(document.getElementById("mn").value);
                var out = document.getElementById("mans");
                if (a === null || b === null || n === null) { out.value = "Please enter whole numbers only."; return; }
                if (/^0+$/.test(n)) { out.value = "n must be greater than 0."; return; }
                if (HAS_BIGINT) {
                    var p = BigInt(a) * BigInt(b);
                    out.value = p.toString() + " mod " + n + " = " + (p % BigInt(n)).toString();
                } else if (Number(a) * Number(b) <= 9007199254740991) {
                    var q = Number(a) * Number(b);
                    out.value = q + " mod " + n + " = " + (q % Number(n));
                } else {
                    out.value = "Numbers too large for this browser.";
                }
            };
        </script>
    </body>
</html>
