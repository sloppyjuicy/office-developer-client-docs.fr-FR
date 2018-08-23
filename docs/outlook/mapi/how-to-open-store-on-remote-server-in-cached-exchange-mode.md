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
# <a name="open-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Ouverture d’un magasin sur le serveur distant lorsque Outlook est en Mode Exchange mis en cache

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Cette rubrique contient un exemple de code en langage C++ qui montre comment utiliser l’indicateur **MDB_ONLINE** pour ouvrir une banque de messages sur le serveur distant lorsque Microsoft Outlook 2010 ou Microsoft Outlook 2013 est en Mode Exchange mis en cache. 
  
Le Mode Exchange mis en cache permet d’Outlook 2010 et Outlook 2013 pour utiliser une copie locale de boîte aux lettres d’un utilisateur pendant une connexion avec une copie distante de boîte aux lettres de l’utilisateur sur le serveur Exchange distant tient à jour Outlook 2010 ou Outlook 2013. Lorsque Outlook 2010 ou Outlook 2013 s’exécute en Mode Exchange mis en cache, par défaut, les solutions MAPI qui se connectent à la même session sont également connectées à la banque de messages mis en cache. Toutes les données accessibles et les modifications apportées sont effectuées sur la copie locale de la boîte aux lettres.
  
Un client ou fournisseur de services peut remplacer la connexion à la base de messages locale et ouvrez le magasin sur le serveur distant en définissant le bit pour **MDB_ONLINE** dans le paramètre *ulFlags* lors de l’appel [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md). Une fois que la banque a été ouvert avec succès sur le serveur distant pour cette session, vous pouvez utiliser [IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir des éléments ou des dossiers dans le magasin distant. 
  
Impossible d’ouvrir une banque Exchange en mode mis en cache et en mode non mis en cache en même temps dans la même session MAPI. Si vous avez déjà ouvert la banque de messages mis en cache, vous devez soit fermer le magasin avant d’ouvrir avec cet indicateur ou ouvrir une nouvelle session MAPI où vous pouvez ouvrir la banque d’informations Exchange sur le serveur distant à l’aide de cet indicateur.
  
L’exemple de code suivant montre comment appeler **IMAPISession::OpenMsgStore** avec l’indicateur **MDB_ONLINE** dans le paramètre *ulFlags* pour ouvrir la banque par défaut sur le serveur distant. 
  
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

## <a name="see-also"></a>Voir aussi

- [À propos des ajouts MAPI](about-mapi-additions.md) 
- [Constantes MAPI](mapi-constants.md)
- [Accès à un magasin sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)

