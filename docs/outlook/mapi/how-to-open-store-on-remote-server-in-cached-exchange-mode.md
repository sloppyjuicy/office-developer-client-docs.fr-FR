---
title: Ouvrir un magasin sur le serveur distant lorsque Outlook est en mode cache Exchange
description: Cet article explique comment ouvrir un magasin sur le serveur distant lorsque Outlook est en mode cache Exchange avec syntaxe.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: cf01eab7-164d-c3b3-8bb0-9281e2119bc5
ms.openlocfilehash: 6b5ed1fb89dc652f4bc7014b328ad3300c120bad
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817493"
---
# <a name="open-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Ouvrir un magasin sur le serveur distant lorsque Outlook est en mode cache Exchange

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique contient un exemple de code en C++ qui montre comment utiliser l’indicateur **de MDB_ONLINE** pour ouvrir un magasin de messages sur le serveur distant lorsque Microsoft Outlook 2010 ou Microsoft Outlook 2013 est en mode mis en cache Exchange. 
  
Le mode Exchange mis en cache permet Outlook 2010 et Outlook 2013 d’utiliser une copie locale de la boîte aux lettres d’un utilisateur pendant que Outlook 2010 ou Outlook 2013 conserve une connexion en ligne à une copie à distance de la boîte aux lettres de l’utilisateur sur le serveur Exchange distant. Lorsque Outlook 2010 ou Outlook 2013 s’exécute en mode Exchange mis en cache, par défaut, toutes les solutions MAPI qui se connectent à la même session sont également connectées au magasin de messages mis en cache. Toutes les données accessibles et toutes les modifications apportées sont apportées à la copie locale de la boîte aux lettres.
  
Un client ou un fournisseur de services peut remplacer la connexion au magasin de messages local et ouvrir le magasin sur le serveur distant en définissant le bit pour **MDB_ONLINE** dans le paramètre  *ulFlags*  lors de [l’appel d’IMAPISession::OpenMsgStore](imapisession-openmsgstore.md). Une fois le magasin ouvert sur le serveur distant pour cette session, vous pouvez utiliser [IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir des éléments ou des dossiers sur le magasin distant. 
  
Vous ne pouvez pas ouvrir un magasin Exchange en mode mis en cache et en mode non mis en cache en même temps dans la même session MAPI. Si vous avez déjà ouvert la banque de messages mise en cache, vous devez fermer la banque avant de l’ouvrir avec cet indicateur, ou ouvrir une nouvelle session MAPI où vous pouvez ouvrir la banque d'informations Exchange sur le serveur distant à l’aide de cet indicateur.
  
L’exemple de code suivant montre comment appeler **IMAPISession::OpenMsgStore** avec l’indicateur **MDB_ONLINE** défini dans le paramètre  *ulFlags*  pour ouvrir le magasin par défaut sur le serveur distant. 
  
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
- [Accès à une banque sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)

