---
title: IAddrBookAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Address
api_type:
- COM
ms.assetid: ef2112c7-35cd-4106-ad18-a45e1dbe07d6
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a13696b355e6fd815cd6bda42843505d9fc3d1f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579955"
---
# <a name="iaddrbookaddress"></a>IAddrBook::Address

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Affiche la boîte de dialogue de carnet d’adresse Outlook. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Paramètres

 _lpulUIParam_
  
> [entrée, sortie] Pointeur vers un handle de la fenêtre parent de la boîte de dialogue. À l’entrée, un handle de fenêtre doit toujours être transmis. Dans la sortie, si le membre **ulFlags** du paramètre _lpAdrParms_ est défini sur DIALOG_SDI, le handle de fenêtre de la boîte de dialogue non modale est renvoyé. Voir les remarques. 
    
 _lpAdrParms_
  
> [entrée, sortie] Un pointeur vers une structure [ADRPARM](adrparm.md) qui contrôle la présentation et le comportement de la boîte de dialogue adresses. 
    
 _lppAdrList_
  
> [entrée, sortie] Pointeur vers un pointeur vers une structure [ADRLIST](adrlist.md) qui contient les informations relatives au destinataire. À l’entrée, ce paramètre peut être NULL ou pointez sur un pointeur valide. Dans la sortie, ce paramètre pointe vers un pointeur vers les informations relatives au destinataire valides. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La boîte de dialogue adresse a été correctement affichée.
    
## <a name="remarks"></a>Remarques

Si le membre **ulFlags** du paramètre _lpAdrParms_ est défini sur DIALOG_SDI anticipation le retour de handle de fenêtre de la boîte de dialogue non modale en sortie, il est ignoré dans Outlook ; la version de la boîte de dialogue modale est toujours affichée dans les clients non Outlook. 
  
La structure **ADRLIST** transmise par MAPI à l’appelant via le paramètre _lppAdrList_ contient un tableau de structures [ADRENTRY](adrentry.md) , une structure pour chaque destinataire. Lorsqu’il est passé à la méthode de [IMessage::ModifyRecipients](imessage-modifyrecipients.md) d’un message sortant dans le paramètre _lpMods_ , la structure **ADRLIST** peut être utilisée pour mettre à jour sa liste de destinataires. 
  
Chaque structure **ADRENTRY** dans la structure **ADRLIST** contient zéro ou plusieurs structures [SPropValue](spropvalue.md) , une structure pour chaque propriété définie pour le destinataire. Il peut être zéro structures **SPropValue** lorsque la boîte de dialogue présentée par la méthode **adresse** est utilisée pour supprimer un destinataire. Lorsqu’il existe une ou plusieurs structures **SPropValue** , la structure **ADRENTRY** correspondante est utilisée pour ajouter ou mettre à jour d’un destinataire. Le destinataire peut être résolu, ce qui indique qu’une des structures **SPropValue** décrit la propriété du destinataire **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), ou non résolus, qui indique que la propriété **PR_ENTRYID** est manquante. 
  
Outre **PR_ENTRYID**, destinataires résolus comprennent les propriétés suivantes :
  
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
La structure **ADRLIST** qui transmet l’appelant peut être une taille différente de la structure renvoie MAPI. Si MAPI doit renvoyer une plus grande structure **ADRLIST** , il libère la structure d’origine et alloue un nouveau. Lorsque vous affectez la mémoire pour la structure **ADRLIST** , allouer la mémoire pour chaque structure **SPropValue** séparément. Pour plus d’informations sur la façon d’allouer et libérer les structures **ADRLIST** , voir [Gestion de la mémoire ADRLIST des Structures SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)
  
 **Adresse** renvoie immédiatement si l’indicateur DIALOG_SDI est défini dans le membre **ulFlags** de la structure **ADRPARM** dans le paramètre _lpAdrParms_ . L’indicateur DIALOG_SDI est ignorée pour les clients non Outlook. Si DIALOG_SDI est ignorée, la version de la boîte de dialogue modale s’affiche et un pointeur vers un handle ne doit pas dans _lpulUIParam_.
  
 **Adresse** prend en charge les chaînes de caractères Unicode dans la structure **ADRPARM** si AB_UNICODEUI a été spécifié dans le membre **ulFlags** de **ADRPARM** dans le paramètre _lpAdrParms_ , et il prend en charge les chaînes de caractères Unicode dans ** ADRLIST**. Les chaînes Unicode sont convertis au format de chaîne (MBCS) codés avant qu’elles sont affichées dans la boîte de dialogue de carnet d’adresse Outlook.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |OpenOtherUsersMailboxFromGal  <br/> |MFCMAPI utilise la méthode **adresse** pour autoriser l’utilisateur à sélectionner les boîtes aux lettres à ouvrir.  <br/> |
   
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

