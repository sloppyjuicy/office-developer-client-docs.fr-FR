---
<span data-ttu-id="701a3-101"><<<<<<< Titre tête : Description, HelpContext, HelpFile, propriétés-exemple (VC ++) TOCTitle : Description, HelpContext, HelpFile, NativeError, nombre, Source et SQLState, propriétés-exemple (VC ++) === titre : Description, HelpContext, HelpFile, propriétés-exemple (VC ++) TOCTitle : Description, HelpContext, HelpFile, NativeError, nombre, Source et SQLState, propriétés-exemple (VC ++)</span><span class="sxs-lookup"><span data-stu-id="701a3-101"><<<<<<< HEAD title: Description, HelpContext, HelpFile Properties Example (VC++) TOCTitle: Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState Properties Example (VC++) ======= title: Description, HelpContext, HelpFile properties example (VC++) TOCTitle: Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState properties example (VC++)</span></span>
>>>>>>> <span data-ttu-id="701a3-102">Master ms:assetid : 1375a0e6-c61b-aba5-4d7c-5db597ef873e ms:mtpsurl : https://msdn.microsoft.com/library/JJ248908(v=office.15) ms:contentKeyID : ms.date 48543369 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="701a3-102">master ms:assetid: 1375a0e6-c61b-aba5-4d7c-5db597ef873e ms:mtpsurl: https://msdn.microsoft.com/library/JJ248908(v=office.15) ms:contentKeyID: 48543369 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="701a3-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="701a3-103"><<<<<<< HEAD</span></span>
# <a name="description-helpcontext-helpfile-nativeerror-number-source-and-sqlstate-properties-example-vc"></a><span data-ttu-id="701a3-104">Description, HelpContext, HelpFile, NativeError, Number, Source et SQLState, propriétés - Exemple (VC++)</span><span class="sxs-lookup"><span data-stu-id="701a3-104">Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState Properties Example (VC++)</span></span>
=======
# <a name="description-helpcontext-helpfile-nativeerror-number-source-and-sqlstate-properties-example-vc"></a><span data-ttu-id="701a3-105">Description, HelpContext, HelpFile, NativeError, nombre, Source et SQLState, propriétés-exemple (VC ++)</span><span class="sxs-lookup"><span data-stu-id="701a3-105">Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState properties example (VC++)</span></span>
>>>>>>> <span data-ttu-id="701a3-106">master</span><span class="sxs-lookup"><span data-stu-id="701a3-106">master</span></span>


<span data-ttu-id="701a3-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="701a3-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="701a3-108">Cet exemple déclenche une erreur, l'intercepte et affiche les propriétés [Description](description-property-ado.md), [HelpContext](helpcontext-helpfile-properties-ado.md), [HelpFile](helpcontext-helpfile-properties-ado.md), [NativeError](nativeerror-property-ado.md), [Number](number-property-ado.md), [Source](source-property-ado-error.md) et [SQLState](sqlstate-property-ado.md) de l'objet [Error](error-object-ado.md) qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="701a3-108">This example triggers an error, traps it, and displays the [Description](description-property-ado.md), [HelpContext](helpcontext-helpfile-properties-ado.md), [HelpFile](helpcontext-helpfile-properties-ado.md), [NativeError](nativeerror-property-ado.md), [Number](number-property-ado.md), [Source](source-property-ado-error.md), and [SQLState](sqlstate-property-ado.md) properties of the resulting [Error](error-object-ado.md) object.</span></span>

```cpp
    // BeginDescriptionCpp
    #import "C:\Program Files\Common Files\System\ADO\msado15.dll"     no_namespace rename("EOF", "EndOfFile")
    
    #include <ole2.h>
    #include <stdio.h>
    #include<conio.h>
    
    // Function declarations
    inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);};
    void DescriptionX(void);
    void PrintProviderError(_ConnectionPtr pConnection);
    void PrintComError(_com_error &e);
    
    ///////////////////////////////////////////////////////////
    //                                                       //
    //      Main Function                                    //
    //                                                       //
    ///////////////////////////////////////////////////////////
    
    void main()
    {
        if(FAILED(::CoInitialize(NULL)))
            return;
    
        DescriptionX();
    
        //Wait here for user to see the output..
        printf("\nPress any key to continue...");
        getch();
        ::CoUninitialize();
    }
    
    ///////////////////////////////////////////////////////////
    //                                                       //
    //      DescriptionX Function                            //
    //                                                       //
    ///////////////////////////////////////////////////////////
    
    void DescriptionX()
    {
        // Define ADO object pointers.
        // Initialize pointers on define.
        // These are in the ADODB::  namespace
        _ConnectionPtr pConnection = NULL;
        ErrorPtr errorLoop = NULL;
    
        //Define Other Variables
        HRESULT hr = S_OK;
        
    
        try
        {
            // Intentionally trigger an error.
            // open connection
            TESTHR(pConnection.CreateInstance(__uuidof(Connection)));
    
            if (FAILED(hr = pConnection->Open("nothing","","",adConnectUnspecified)))
            {
                _com_issue_error(hr);
                exit(1);
            }
    
            // Cleanup object before exit.
            pConnection->Close();
        }
        catch(_com_error)
        {
            // Pass a connection pointer.
            PrintProviderError(pConnection);
        }
    }
    
    ///////////////////////////////////////////////////////////
    //                                                       //
    //      PrintProviderError Function                      //
    //                                                       //
    ///////////////////////////////////////////////////////////
    
    void PrintProviderError(_ConnectionPtr pConnection)
    {
        //Define Other Variables
        HRESULT  hr = S_OK;
        _bstr_t  strError;
        ErrorPtr  pErr = NULL;
    
        try
        {
            // Enumerate Errors collection and display
            // properties of each Error object.
            long nCount = pConnection->Errors->Count;
    
            // Collection ranges from 0 to nCount - 1.
            for(long i = 0; i < nCount; i++)
            {
                pErr = pConnection->Errors->GetItem(i);
                printf("Error #%d\n", pErr->Number);
                printf(" %s\n",(LPCSTR)pErr->Description);
                printf(" (Source: %s)\n",(LPCSTR)pErr->Source);
                printf(" (SQL State: %s)\n",(LPCSTR)pErr->SQLState);
                printf(" (NativeError: %d)\n",(LPCSTR)pErr->NativeError);
                if ((LPCSTR)pErr->GetHelpFile() == NULL)
                {
                    printf("\tNo Help file available\n");
                }
                else
                {
                    printf("\t(HelpFile: %s\n)" ,pErr->HelpFile);
                    printf("\t(HelpContext: %s\n)" , pErr->HelpContext);
                }
            }
        }
        catch(_com_error &e)
        {
            // Notify the user of errors if any.
            PrintComError(e);
        }
    }
    
    ///////////////////////////////////////////////////////////
    //                                                       //
    //      PrintComError Function                           //
    //                                                       //
    ///////////////////////////////////////////////////////////
    
    void PrintComError(_com_error &e)
    {
       // Notify the user of errors if any.
       _bstr_t bstrSource(e.Source());
       _bstr_t bstrDescription(e.Description());
        
        // Print Com errors.
        
       printf("Error\n");
       printf("\tCode = %08lx\n", e.Error());
       printf("\tCode meaning = %s", e.ErrorMessage());
       printf("\tSource = %s\n", (LPCSTR) bstrSource);
       printf("\tDescription = %s\n", (LPCSTR) bstrDescription);
    }
    // EndDescriptionCpp
```
