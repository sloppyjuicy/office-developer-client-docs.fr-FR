---
title: IMAPISupportAddress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Address
api_type:
- COM
ms.assetid: 8c22547e-ddf5-47f7-aed3-76e3854688df
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 7300c11d5835640fe308430c9bb08d40b397e47b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331604"
---
# <a name="imapisupportaddress"></a>IMAPISupport::Address

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Affiche la boîte de dialogue adresse commune. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Paramètres

 _lpulUIParam_
  
> [in, out] Pointeur vers le handle de la fenêtre parente de la boîte de dialogue. Lors de l'entrée, un descripteur de fenêtre doit toujours être passé. Lors de la sortie, si l'indicateur DIALOG_SDI est défini dans la structure [ADRPARM](adrparm.md) vers laquelle pointe le paramètre _lpAdrParms_ , le handle de fenêtre de la boîte de dialogue non modale est renvoyé. 
    
 _lpAdrParms_
  
> [in, out] Pointeur vers une structure **ADRPARM** qui contrôle la présentation et le comportement de la boîte de dialogue d'adresse. 
    
 _lppAdrList_
  
> [in, out] Pointeur vers un pointeur vers une liste d'adresses. Lors de l'entrée, il s'agit de la liste actuelle des destinataires d'un message ou NULL, si cette liste n'existe pas. Lors de la sortie, _lppAdrList_ pointe vers une liste mise à jour des destinataires du message. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La boîte de dialogue adresse s'est affichée.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: Address** est implémentée pour les objets de prise en charge du fournisseur de carnet d'adresses. **Adresses** d'appel des fournisseurs de carnet d'adresses pour créer ou mettre à jour une liste de destinataires de message. 
  
Chaque destinataire est décrit dans une structure [ADRENTRY](adrentry.md) incluse dans la structure [ADRLIST](adrlist.md) désignée par le paramètre _lppAdrList_ . La structure **ADRENTRY** contient un tableau de valeurs de propriété de destinataire, dont l'une est le type du destinataire ou la propriété **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). Cette structure **ADRLIST** peut être transmise à un client pour l'utiliser en tant que paramètre _lpMods_ dans un appel à [IMessage:: ModifyRecipients](imessage-modifyrecipients.md).
  
Chaque destinataire de la structure **ADRLIST** peut être résolu, ce qui indique que l'une de ses valeurs de propriété est sa propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ou non résolu, ce qui indique que la propriété **PR_ENTRYID** est sans. 
  
En plus de la propriété **PR_ENTRYID**, les destinataires résolus incluent les propriétés suivantes:
  
- **PR_RECIPIENT_TYPE**
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
Les destinataires non résolus incluent généralement uniquement **PR_DISPLAY_NAME** et **PR_RECIPIENT_TYPE**. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

La structure **ADRLIST** que l'appelant passe peut avoir une taille différente de celle renvoyée par MAPI. Lorsque vous allouez de la mémoire pour la structure **ADRLIST** , allouez séparément la mémoire pour chaque structure [SPropValue](spropvalue.md) . 
  
Utilisez les pointeurs vers les fonctions d'allocation de mémoire MAPI transmises à votre fonction [ABProviderInit](abproviderinit.md) pour allouer de la mémoire. AlLouez de la mémoire avec la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) pour **ADRLIST** et chaque structure de valeur de propriété dans les structures **ADRENTRY** dans **ADRLIST**. 
  
Si l' **adresse** doit renvoyer une structure **ADRLIST** plus grande, ou si vous avez passé la valeur null pour _lppAdrList_, **Address** libère la structure d'origine et alloue une nouvelle. **Address** alloue également des structures de valeurs de propriétés supplémentaires dans la structure **ADRLIST** et libère les anciennes comme il convient. Pour plus d'informations sur la gestion de la mémoire pour les structures **ADRLIST** , consultez la rubrique [Managing Memory for ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
 L' **adresse** est renvoyée immédiatement si l'indicateur DIALOG_SDI a été défini dans la structure **ADRPARM** dans le paramètre _lpAdrParms_ . 
  
## <a name="see-also"></a>Voir aussi



[ABProviderInit](abproviderinit.md)
  
[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[ADRPARM](adrparm.md)
  
[FreePadrlist](freepadrlist.md)
  
[FreeProws](freeprows.md)
  
[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriété canonique PidTagAddressType](pidtagaddresstype-canonical-property.md)
  
[Propriété canonique PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Propriété canonique PidTagDisplayType](pidtagdisplaytype-canonical-property.md)
  
[Propriété canonique PidTagEntryId](pidtagentryid-canonical-property.md)
  
[Propriété canonique PidTagRecipientType](pidtagrecipienttype-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)


[Gestion de la mémoire pour les structures ADRLIST et SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)

