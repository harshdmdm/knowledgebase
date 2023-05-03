GBT Troubleshooting
====================

Focusser won't Focus
--------------------

.. warning:: TA or OS Only should physically handle the focusser

.. note:: This is very problematic, there are various strategies.

.. note:: Strategy 1: Resetting the Focusser
  
  - Close FocusMax and CCD Soft on the Computer
  - At the telescope, check the focusser is unlocked
  - Use the focus hand control to drive to "physical zero"

    - i.e. there is no gap where the focusser moves outwards
    - ignore whatever value is on the hand controller

  - Unplug focusser - breathe - plug back in
  - Check focusser control now reads 0000
  - Re-open FocusMax

    - Focus should move to last set value
    - Check value in FocusMax
    - Check value matches on manual control

  - Re-try Focus

.. seealso:: There is no promise this works. If focus max attempts to go backwards (i.e. to 9999 and downwards) then you will need to try again.
