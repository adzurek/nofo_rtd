========
OVERVIEW
========

Some sample code.

.. code-block:: csharp

    public async Task CancelCalibration(int deviceId, string operationId)
    {
        var body = new
        {
            DeviceId = deviceId,
            OperationId = operationId
        };
        var response = await _apiClient.PostAsJsonAsync("my/lock/calibrationcancel", body);

        if (!response.IsSuccessStatusCode)
        {
            Console.WriteLine(response.StatusCode);
            return;
        }

        Console.WriteLine("Calibration cancel request has been sent.");
    }


