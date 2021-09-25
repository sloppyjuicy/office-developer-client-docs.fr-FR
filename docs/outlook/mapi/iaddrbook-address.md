---
title: IAddrBookAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.Address
api_type:
- COM
ms.assetid: ef2112c7-35cd-4106-ad18-a45e1dbe07d6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1c4516c081fdd4cd41b1675a41d42957d6d4dd03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592472"
---
# <a name="iaddrbookaddress"></a>IAddrBook::Address

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Affiche la boîte de dialogue Outlook carnet d’adresses. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Paramètres

 _lpulUIParam_
  
> [in, out] Pointeur vers un handle de la fenêtre parente de la boîte de dialogue. Lors de l’entrée, une poignée de fenêtre doit toujours être passée. En sortie, si le membre **ulFlags** du paramètre  _lpAdrParms_ est DIALOG_SDI, le handle de fenêtre de la boîte de dialogue sans mode est renvoyé. Voir les remarques. 
    
 _lpAdrParms_
  
> [in, out] Pointeur vers une structure [ADRPARM](adrparm.md) qui contrôle la présentation et le comportement de la boîte de dialogue d’adresse. 
    
 _lppAdrList_
  
> [in, out] Pointeur vers un pointeur vers une structure [ADRLIST](adrlist.md) qui contient des informations sur le destinataire. Lors de l’entrée, ce paramètre peut être NULL ou pointer vers un pointeur valide. En sortie, ce paramètre pointe vers un pointeur vers des informations de destinataire valides. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La boîte de dialogue d’adresse commune a été affichée avec succès.
    
## <a name="remarks"></a>Remarques

Si le membre **ulFlags** du paramètre _lpAdrParms_ a la valeur DIALOG_SDI anticipant le retour de la poignée de fenêtre de la boîte de dialogue sans mode lors de la sortie, il est ignoré dans Outlook ; La version modale de la boîte de dialogue est toujours affichée dans les clients Outlook non-clients. 
  
La structure **ADRLIST** transmise par MAPI à l’appelant via le paramètre  _lppAdrList_ contient un tableau de structures [ADRENTRY,](adrentry.md) une structure pour chaque destinataire. Lorsqu’elle est transmise à la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) d’un message sortant dans le paramètre  _lpMods,_ la structure **ADRLIST** peut être utilisée pour mettre à jour sa liste des destinataires. 
  
Chaque structure **ADRENTRY** dans la structure **ADRLIST** contient zéro ou plusieurs structures [SPropValue,](spropvalue.md) une structure pour chaque propriété définie pour le destinataire. Il ne peut y avoir aucune structure **SPropValue** lorsque la boîte de dialogue présentée par la méthode **Address** est utilisée pour supprimer un destinataire. Lorsqu’il existe une ou plusieurs structures **SPropValue,** la structure **ADRENTRY** correspondante est utilisée pour ajouter ou mettre à jour un destinataire. Le destinataire peut être résolu, ce qui indique que l’une des structures **SPropValue** décrit la propriété **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)du destinataire, ou non résolue, ce qui indique que la propriété **PR_ENTRYID** est manquante. 
  
En plus de **PR_ENTRYID,** les destinataires résolus incluent les propriétés suivantes :
  
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
La structure **ADRLIST** que l’appelant transmet peut être d’une taille différente de la structure que MAPI renvoie. Si MAPI doit renvoyer une structure **ADRLIST** plus grande, il libère la structure d’origine et en alloue une nouvelle. Lorsque vous allouez de la mémoire pour la structure **ADRLIST,** allouez la mémoire pour chaque structure **SPropValue** séparément. Pour plus d’informations sur l’allocation et la gratuité des structures **ADRLIST,** voir [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)
  
 **L’adresse** renvoie immédiatement si l’DIALOG_SDI est définie dans le membre **ulFlags** de la structure **ADRPARM** dans le paramètre _lpAdrParms._ L DIALOG_SDI est ignoré pour les clients non Outlook client. Si DIALOG_SDI est ignoré, la version modale de la boîte de dialogue s’affiche et un pointeur vers un handle ne doit pas être attendu dans  _lpulUIParam_.
  
 **Address** prend en charge les chaînes de caractères Unicode dans la structure **ADRPARM** si AB_UNICODEUI a été spécifié dans le membre **ulFlags** d’ADRPARM dans le paramètre _lpAdrParms_ et prend en charge les chaînes de caractères Unicode dans **ADRLIST**.  Les chaînes Unicode sont converties au format de chaîne de caractères multioctets (MBCS) avant d’être affichées dans la boîte de dialogue Outlook carnet d’adresses.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |OpenOtherUsersMailboxFromGal  <br/> |MFCMAPI utilise la méthode **Address** pour permettre à l’utilisateur de sélectionner la boîte aux lettres à ouvrir.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[ADRPARM](adrparm.md)
  
[FreePadrlist](freepadrlist.md)
  
[FreeProws](freeprows.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

