Robot-framework-percy for SeleniumLibrary
=====================

.. contents::

Introduction
------------
Robot framework client library for visual regression testing with Percy and  SeleniumLibrary.

Installation
------------

The recommended installation method is using pip::

    pip install git+https://github.com/carlosnizolli/robot-framework-percy.git

Usage
-----

.. code:: robotframework

    *** Settings ***
    Library    RobotFrameworkPercy


    *** Keywords ***
    Initialize
        Open Browser              url    Chrome

        # initialize percy
        Percy Initialize Build    access_token=${PERCY_TOKEN}

    Take Snapshot
        # take snapshot
        Percy Snapshot    snapshot name

    Teardown
        # finalize and push to percy server
        Percy Finalize Build

