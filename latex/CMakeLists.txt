cmake_minimum_required( VERSION 2.8 )
project( msc-thesis )
include( "${CMAKE_SOURCE_DIR}/UseLATEX.cmake" )

file( GLOB paper_sources RELATIVE ${CMAKE_SOURCE_DIR}
  bib/*.bib
  tex/*.tex
  tex/static/*.tex
  fig/*.png
)

ADD_LATEX_DOCUMENT(
  msc-thesis.tex
  INPUTS ${paper_sources}
  BIBFILES bib/bibliography.bib
)
