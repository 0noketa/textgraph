! TextGraph

TextGraph is a parser for ascii-art graphs.

http://textgraph.rubyforge.org/

!! Example

*----*   *---*
|foo +--->bar|
*-+--*   *---*
  |
 *v---*
 |baz |
 *----*

>> require 'textgraph'
=> true
>> graph = TextGraph.parse(File.read("b.zu"))
=> #<TextGraph::Graph:0x2b4fc09a19c0 @links=[[0, 1], [0, 2]],
     @cells=[#<TextGraph::Cell:0x2b4fc099c538 @y=0, @raw_content="foo ",
     @x=0, @h=3, @w=6>, #<TextGraph::Cell:0x2b4fc099b8b8 @y=0, 
     @raw_content="bar", @x=9, @h=3, @w=5>,
     #<TextGraph::Cell:0x2b4fc0999ab8 @y=4, @raw_content="baz ", @x=1,
     @h=3, @w=6>]
>> graph.cells
=> [#<TextGraph::Cell:0x2b4fc099c538 @y=0, @raw_content="foo ", @x=0, @h=3, @w=6>,
    #<TextGraph::Cell:0x2b4fc099b8b8 @y=0, @raw_content="bar", @x=9, @h=3, @w=5>,
    #<TextGraph::Cell:0x2b4fc0999ab8 @y=4, @raw_content="baz ", @x=1, @h=3, @w=6>]
>> graph.links
=> [[0, 1], [0, 2]]

!! Licence

Ruby's

!! History

* 0.1.0 2007-09-28
** Initial release

!! Author
yhara(Yutaka HARA) / yhara(at)kmc.gr.jp
http://mono.kmc.gr.jp/~yhara/
