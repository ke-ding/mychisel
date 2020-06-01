# mychisel
chisel projects start point

To generate verilog:
import chisel3.stage._
(new chisel3.stage.ChiselStage).execute(
    Array("-X", "verilog", "-td", "out"),
    Seq( ChiselGeneratorAnnotation(() => new gcd.GCD()) )
)

To print (and gen) verilog:
import chisel3.stage._
(new ChiselStage).emitVerilog(new gcd.GCD(), Array("-td", "out"))

