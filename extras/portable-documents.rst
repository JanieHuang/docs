==================
Creating PDF files
==================

The OxyPlot core library contains a class ``PortableDocument`` that can be used to create PDF files:

.. code:: csharp

    var file = File.Create("HelloWorld.pdf");
    var doc = new PortableDocument();
    doc.Title = "Hello world";
    doc.Author = "objo";
    doc.AddPage(PageSize.A4);
    doc.SetFont("Arial", 96);
    doc.DrawText(50, 400, "Hello world!");
    doc.Save(file);

Note that the coordinate system origin is at the bottom left corner of the page and the unit is point (1/72 inch).

The ``PortableDocument`` class supports

- document properties (title, author, subject etc.)
- multiple pages (specify size and orientation)
- text drawing
- Type 1 fonts (Helvetica, Roman, Courier) in WinAnsi encoding
- text size measuring
- circles
- ellipses
- lines
- polygons
- rectangles
- images
- clipping rectangle
- transforms
- transparency

More examples can be found in the unit tests in ``Source\OxyPlot.Tests\Pdf\PortableDocumentTests.cs``
