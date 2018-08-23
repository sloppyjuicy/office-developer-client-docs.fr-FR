---
title: Ouverture d’un magasin sur le serveur distant lorsque Outlook est en Mode Exchange mis en cache
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf01eab7-164d-c3b3-8bb0-9281e2119bc5
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: 7c1b3d3d5eed6bc991f8e4fd702fa197d610c104
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584799"
---
# <a name="open-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a><span data-ttu-id="86967-103">Ouverture d’un magasin sur le serveur distant lorsque Outlook est en Mode Exchange mis en cache</span><span class="sxs-lookup"><span data-stu-id="86967-103">Open a store on the remote server when Outlook is in Cached Exchange Mode</span></span>

<span data-ttu-id="86967-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86967-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86967-105">Cette rubrique contient un exemple de code en langage C++ qui montre comment utiliser l’indicateur **MDB_ONLINE** pour ouvrir une banque de messages sur le serveur distant lorsque Microsoft Outlook 2010 ou Microsoft Outlook 2013 est en Mode Exchange mis en cache.</span><span class="sxs-lookup"><span data-stu-id="86967-105">This topic contains a code sample in C++ that shows how to use the **MDB_ONLINE** flag to open a message store on the remote server when Microsoft Outlook 2010 or Microsoft Outlook 2013 is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="86967-106">Le Mode Exchange mis en cache permet d’Outlook 2010 et Outlook 2013 pour utiliser une copie locale de boîte aux lettres d’un utilisateur pendant une connexion avec une copie distante de boîte aux lettres de l’utilisateur sur le serveur Exchange distant tient à jour Outlook 2010 ou Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="86967-106">Cached Exchange Mode permits Outlook 2010 and Outlook 2013 to use a local copy of a user's mailbox while Outlook 2010 or Outlook 2013 maintains an online connection to a remote copy of the user's mailbox on the remote Exchange server.</span></span> <span data-ttu-id="86967-107">Lorsque Outlook 2010 ou Outlook 2013 s’exécute en Mode Exchange mis en cache, par défaut, les solutions MAPI qui se connectent à la même session sont également connectées à la banque de messages mis en cache.</span><span class="sxs-lookup"><span data-stu-id="86967-107">When Outlook 2010 or Outlook 2013 is running in Cached Exchange Mode, by default, any MAPI solutions that log on to the same session are also connected to the cached message store.</span></span> <span data-ttu-id="86967-108">Toutes les données accessibles et les modifications apportées sont effectuées sur la copie locale de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="86967-108">Any data that is accessed and any changes that are made are made against the local copy of the mailbox.</span></span>
  
<span data-ttu-id="86967-109">Un client ou fournisseur de services peut remplacer la connexion à la base de messages locale et ouvrez le magasin sur le serveur distant en définissant le bit pour **MDB_ONLINE** dans le paramètre *ulFlags* lors de l’appel [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span><span class="sxs-lookup"><span data-stu-id="86967-109">A client or service provider can override the connection to the local message store and open the store on the remote server by setting the bit for **MDB_ONLINE** in the  *ulFlags*  parameter when calling [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span> <span data-ttu-id="86967-110">Une fois que la banque a été ouvert avec succès sur le serveur distant pour cette session, vous pouvez utiliser [IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir des éléments ou des dossiers dans le magasin distant.</span><span class="sxs-lookup"><span data-stu-id="86967-110">After the store has been successfully opened on the remote server for that session, you can use [IMAPISession::OpenEntry](imapisession-openentry.md) to open items or folders on the remote store.</span></span> 
  
<span data-ttu-id="86967-111">Impossible d’ouvrir une banque Exchange en mode mis en cache et en mode non mis en cache en même temps dans la même session MAPI.</span><span class="sxs-lookup"><span data-stu-id="86967-111">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="86967-112">Si vous avez déjà ouvert la banque de messages mis en cache, vous devez soit fermer le magasin avant d’ouvrir avec cet indicateur ou ouvrir une nouvelle session MAPI où vous pouvez ouvrir la banque d’informations Exchange sur le serveur distant à l’aide de cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="86967-112">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
  
<span data-ttu-id="86967-113">L’exemple de code suivant montre comment appeler **IMAPISession::OpenMsgStore** avec l’indicateur **MDB_ONLINE** dans le paramètre *ulFlags* pour ouvrir la banque par défaut sur le serveur distant.</span><span class="sxs-lookup"><span data-stu-id="86967-113">The following code sample shows how to call **IMAPISession::OpenMsgStore** with the **MDB_ONLINE** flag set in the  *ulFlags*  parameter to open the default store on the remote server.</span></span> 
  
```cpp
HRESULT HrRemoteMessageStore( 
    LPMAPISESSION lpMAPISession, 
    LPMDB* lppMDB) 
{ 
    HRESULT hRes = S_OK; 
    LPMAPITABLE pStoresTbl = NULL; 
    SRestriction sres = {0}; 
    SPropValue spv = {0}; 
    LPSRowSet pRow = NULL; 
    LPMDB lpTempMDB = NULL; 
    enum {EID,NUM_COLS}; 
    static SizedSPropTagArray(NUM_COLS,sptCols) = {NUM_COLS, 
        PR_ENTRYID, 
    }; 
 
    //Obtain the table of all the message stores that are available 
    hRes = lpMAPISession-&gt;GetMsgStoresTable(0, &amp;pStoresTbl); 
     
    if (SUCCEEDED(hRes) &amp;&amp; pStoresTbl) 
    { 
        //Set up restrictions for the default store 
        sres.rt = RES_PROPERTY;                                  //Comparing a property 
        sres.res.resProperty.relop = RELOP_EQ;                   //Testing equality 
        sres.res.resProperty.ulPropTag = PR_DEFAULT_STORE;       //Tag to compare 
        sres.res.resProperty.lpProp = &amp;spv;                      //Prop tag and value to compare against 
     
        spv.ulPropTag = PR_DEFAULT_STORE;                        //Tag type 
        spv.Value.b   = TRUE;                                    //Tag value 
     
        //Convert the table to an array that can be stepped through 
        //Only one message store should have PR_DEFAULT_STORE set to true, so that only one will be returned 
        hRes = HrQueryAllRows( 
            pStoresTbl,                                          //Table to query 
            (LPSPropTagArray) &amp;sptCols,                          //Which columns to obtain 
            &amp;sres,                                               //Restriction to use 
            NULL,                                                //No sort order 
            0,                                                   //Max number of rows (0 means no limit) 
            &amp;pRow);                                              //Array to return 
 
        if (SUCCEEDED(hRes) &amp;&amp; pRow &amp;&amp; pRow-&gt;cRows) 
        {     
            //Open the first returned (default) message store 
            hRes = lpMAPISession-&gt;OpenMsgStore( 
                NULL,                                                //Window handle for dialogs 
                pRow-&gt;aRow[0].lpProps[EID].Value.bin.cb,             //size and... 
                (LPENTRYID)pRow-&gt;aRow[0].lpProps[EID].Value.bin.lpb, //value of entry to open 
                NULL,                                                //Use default interface (IMsgStore) to open store 
                MAPI_BEST_ACCESS | MDB_ONLINE,                       //Flags 
                &amp;lpTempMDB);                                         //Pointer to put the store in 
            if (SUCCEEDED(hRes) &amp;&amp; lppMDB) lppMDB* = lpTempMDB; 
        } 
    } 
    FreeProws(pRow); 
    if (pStoresTbl) pStoresTbl-&gt;Release(); 
 
    return hRes; 
}

```

## <a name="see-also"></a><span data-ttu-id="86967-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86967-114">See also</span></span>

- [<span data-ttu-id="86967-115">À propos des ajouts MAPI</span><span class="sxs-lookup"><span data-stu-id="86967-115">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="86967-116">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="86967-116">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="86967-117">Accès à un magasin sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache</span><span class="sxs-lookup"><span data-stu-id="86967-117">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)

