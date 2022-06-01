---
title: IAddrBookAddress
description: Cet article décrit la fonction IAddrBookAddress et fournit la syntaxe, les paramètres et la valeur de retour.
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
ms.openlocfilehash: 835ebfc49c24040dd15a68c41a232cbe73ee5562
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816877"
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
  
> [in, out] Pointeur vers un handle de la fenêtre parente de la boîte de dialogue. Lors de l’entrée, un handle de fenêtre doit toujours être passé. En sortie, si le membre **ulFlags** du paramètre  _lpAdrParms_ est défini sur DIALOG_SDI, le handle de fenêtre de la boîte de dialogue sans mode est retourné. Voir les remarques. 
    
 _lpAdrParms_
  
> [in, out] Pointeur vers une structure [ADRPARM](adrparm.md) qui contrôle la présentation et le comportement de la boîte de dialogue d’adresse. 
    
 _lppAdrList_
  
> [in, out] Pointeur vers un pointeur vers une structure [ADRLIST](adrlist.md) qui contient des informations sur le destinataire. Lors de l’entrée, ce paramètre peut être NULL ou pointer vers un pointeur valide. Lors de la sortie, ce paramètre pointe vers un pointeur vers des informations de destinataire valides. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La boîte de dialogue d’adresse commune a été affichée avec succès.
    
## <a name="remarks"></a>Remarques

Si le membre **ulFlags** du paramètre _lpAdrParms_ est défini sur DIALOG_SDI anticiper le retour du handle de fenêtre de la boîte de dialogue sans mode lors de la sortie, il est ignoré dans Outlook ; la version modale de la boîte de dialogue est toujours affichée dans les clients non Outlook. 
  
La structure **ADRLIST** passée par MAPI à l’appelant via le paramètre  _lppAdrList_ contient un tableau de structures [ADRENTRY](adrentry.md) , une structure pour chaque destinataire. Lorsqu’elle est passée à la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) d’un message sortant dans le paramètre _lpMods_ , la structure **ADRLIST** peut être utilisée pour mettre à jour sa liste de destinataires. 
  
Chaque structure **ADRENTRY** de la structure **ADRLIST** contient zéro ou plusieurs structures [SPropValue](spropvalue.md) , une structure pour chaque ensemble de propriétés pour le destinataire. Il peut y avoir zéro structure **SPropValue** lorsque la boîte de dialogue présentée par la méthode **Address** est utilisée pour supprimer un destinataire. Lorsqu’il existe une ou plusieurs structures **SPropValue** , la structure **ADRENTRY** correspondante est utilisée pour ajouter ou mettre à jour un destinataire. Le destinataire peut être résolu, ce qui indique que l’une des structures **SPropValue** décrit la propriété **PR_ENTRYID** du destinataire ([PidTagEntryId](pidtagentryid-canonical-property.md)) ou non résolue, ce qui indique que la propriété **PR_ENTRYID** est manquante. 
  
Outre **PR_ENTRYID**, les destinataires résolus incluent les propriétés suivantes :
  
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
La structure **ADRLIST** que l’appelant transmet peut être d’une taille différente de celle retournée par MAPI. Si MAPI doit retourner une structure **ADRLIST** plus grande, elle libère la structure d’origine et en alloue une nouvelle. Lorsque vous allouez de la mémoire pour la structure **ADRLIST** , allouez la mémoire pour chaque structure **SPropValue** séparément. Pour plus d’informations sur l’allocation et la gratuité des structures **ADRLIST** , consultez [Gestion de la mémoire pour les structures ADRLIST et SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)
  
 **L’adresse** retourne immédiatement si l’indicateur DIALOG_SDI est défini dans le membre **ulFlags** de la structure **ADRPARM** dans le paramètre _lpAdrParms_ . L’indicateur DIALOG_SDI est ignoré pour les clients non Outlook. Si DIALOG_SDI est ignoré, la version modale de la boîte de dialogue s’affiche et un pointeur vers un handle ne doit pas être attendu dans  _lpulUIParam_.
  
 **Address** prend en charge les chaînes de caractères Unicode dans la structure **ADRPARM** si AB_UNICODEUI a été spécifié dans le membre **ulFlags** **d’ADRPARM** dans le paramètre _lpAdrParms_ , et prend en charge les chaînes de caractères Unicode dans **ADRLIST**. Les chaînes Unicode sont converties au format de chaîne de caractères multioctets (MBCS) avant d’être affichées dans la boîte de dialogue Outlook carnet d’adresses.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |OpenOtherUsersMailboxFromGal  <br/> |MFCMAPI utilise la méthode **Address** pour permettre à l’utilisateur de sélectionner la boîte aux lettres à ouvrir. |
   
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

