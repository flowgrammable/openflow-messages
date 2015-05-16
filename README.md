This is a library of torture test messages for OpenFlow testing. You can use
these messages to validate a message layer implementation of the OpenFlow
protocol or to do general testing of a target OpenFlow system. There is a
directory for each version of OpenFlow, which contains torture messages specific
to that version. Each versioned directory contains two subdirectories: rep, and
abs. The rep directory contains representational tests, while the abs directory
contains abstract domain tests.

Each file is a binary blob representing a signle valid or invalid OpenFlow 
message. The extension '.pass' indicates validity, while the extension '.fail'
indicates invalidity. Each filename is split into three sections: test type,
openflow packet type, and test number. A rep test focuses on structural
constraints of a message, while an abs tests focuses on semantic constraints of
a message. The openflow message type is the OpenFlow header type value, and
indicates what type of message: 'EchoReq', 'EchoRes', etc. Finally, the test
number is increasing index of the test.


Use the following naming convention:
    testType_packetTypeNumber_index.expectedResult

    Example: barrier reply packet that should pass representational test
             rep_19_00001.pass
