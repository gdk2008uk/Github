Github
======

Jockey crashes

Application: python2 (0.5.7)
KDE Platform Version: 4.8.3 (4.8.3)
Qt Version: 4.8.1
Operating System: Linux 3.2.0-23-generic i686
Distribution: Linux Mint 13 Maya

-- Information about the crash:
<In detail, tell us what you were doing  when the application crashed.>

The crash can be reproduced every time.

-- Backtrace:
Application: Jockey (python2.7), signal: Segmentation fault
Using host libthread_db library "/lib/i386-linux-gnu/libthread_db.so.1".
[KCrash Handler]
#7  0x043df09c in QWidgetPrivate::deleteTLSysExtra (this=0x9cffcf0) at kernel/qwidget_x11.cpp:2888
#8  0x0438ae37 in QWidgetPrivate::deleteExtra (this=0x9cffcf0) at kernel/qwidget.cpp:1829
#9  0x0438b05c in QWidgetPrivate::~QWidgetPrivate (this=0x9cffcf0, __in_chrg=<optimized out>) at kernel/qwidget.cpp:357
#10 0x04874aa6 in ~QDialogPrivate (this=0x9cffcf0, __in_chrg=<optimized out>) at ../../include/QtGui/private/../../../src/gui/dialogs/qdialog_p.h:66
#11 QDialogPrivate::~QDialogPrivate (this=0x9cffcf0, __in_chrg=<optimized out>) at ../../include/QtGui/private/../../../src/gui/dialogs/qdialog_p.h:66
#12 0x00fd74bb in cleanup (pointer=<optimized out>) at ../../include/QtCore/../../src/corelib/tools/qscopedpointer.h:62
#13 ~QScopedPointer (this=0x9d822c4, __in_chrg=<optimized out>) at ../../include/QtCore/../../src/corelib/tools/qscopedpointer.h:100
#14 QObject::~QObject (this=0x9d822c0, __in_chrg=<optimized out>) at kernel/qobject.cpp:817
#15 0x0438d22d in QWidget::~QWidget (this=0x9d822c0, __in_chrg=<optimized out>) at kernel/qwidget.cpp:1551
#16 0x0488a525 in QDialog::~QDialog (this=0x9d822c0, __in_chrg=<optimized out>) at dialogs/qdialog.cpp:318
#17 0x03aec759 in sipQDialog::~sipQDialog (this=0x9d822c0, __in_chrg=<optimized out>) at sipQtGuipart9.cpp:56047
#18 0x03aec79a in sipQDialog::~sipQDialog (this=0x9d822c0, __in_chrg=<optimized out>) at sipQtGuipart9.cpp:56050
#19 0x00fd1d11 in QObjectPrivate::deleteChildren (this=0x9cae4e8) at kernel/qobject.cpp:1908
#20 0x0438d17c in QWidget::~QWidget (this=0x9cae498, __in_chrg=<optimized out>) at kernel/qwidget.cpp:1676
#21 0x0488a525 in QDialog::~QDialog (this=0x9cae498, __in_chrg=<optimized out>) at dialogs/qdialog.cpp:318
#22 0x03aec759 in sipQDialog::~sipQDialog (this=0x9cae498, __in_chrg=<optimized out>) at sipQtGuipart9.cpp:56047
#23 0x03aec79a in sipQDialog::~sipQDialog (this=0x9cae498, __in_chrg=<optimized out>) at sipQtGuipart9.cpp:56050
#24 0x03ae2863 in release_QDialog (sipCppV=0x9cae498) at sipQtGuipart9.cpp:57688
#25 0x03afa5ec in dealloc_QDialog (sipSelf=0x9a4f2b4) at sipQtGuipart9.cpp:57704
#26 dealloc_QDialog (sipSelf=0x9a4f2b4) at sipQtGuipart9.cpp:57697
#27 0x0032931e in forgetObject (sw=0x9a4f2b4) at /build/buildd/sip4-4.13.2/siplib/siplib.c:10124
#28 0x00329c61 in sipWrapper_dealloc (self=0x9a4f2b4) at /build/buildd/sip4-4.13.2/siplib/siplib.c:9675
#29 0x08108c3f in subtype_dealloc.25423 ()
#30 0x08175d63 in dict_dealloc.18187 ()
#31 0x081089db in subtype_dealloc.25423 ()
#32 0x0815d558 in insertdict.18214 ()
#33 0x0812da30 in PyDict_SetItem ()
#34 0x0807b10d in _PyModule_Clear ()
#35 0x0807b63c in PyImport_Cleanup ()
#36 0x0807bbd7 in Py_Finalize ()
#37 0x080a97c5 in Py_Main ()
#38 0x0805ea5b in main ()
