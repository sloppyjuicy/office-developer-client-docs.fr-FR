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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 524bbfe5f40a66585fb4ed4463b057ca6a0c881a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586801"
---
# <a name="imapisupportaddress"></a>IMAPISupport::Address

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Affiche la boîte de dialogue adresses. 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>Paramètres

 _lpulUIParam_
  
> [entrée, sortie] Pointeur vers le handle de la fenêtre parente de la boîte de dialogue. À l’entrée, un handle de fenêtre doit toujours être transmis. Dans la sortie, si l’indicateur DIALOG_SDI est défini dans la structure [ADRPARM](adrparm.md) désignée par le paramètre _lpAdrParms_ , le handle de fenêtre de la boîte de dialogue non modale est renvoyé. 
    
 _lpAdrParms_
  
> [entrée, sortie] Un pointeur vers une structure **ADRPARM** qui contrôle la présentation et le comportement de la boîte de dialogue adresses. 
    
 _lppAdrList_
  
> [entrée, sortie] Pointeur vers un pointeur vers une liste d’adresses. À l’entrée, cette liste est la liste actuelle des destinataires d’un message ou valeur NULL, si aucune liste de ce type n’existe. Dans la sortie, _lppAdrList_ pointe vers une liste mise à jour de destinataires du message. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La boîte de dialogue adresse a été correctement affichée.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::Address** est implémentée pour les objets de prise en charge du fournisseur adresse téléchargeable. Fournisseurs de carnet d’adresses appellent **adresse** pour créer ou mettre à jour une liste de destinataires du message. 
  
Chaque destinataire est décrite dans une structure [ADRENTRY](adrentry.md) qui est incluse dans la structure [ADRLIST](adrlist.md) désignée par le paramètre _lppAdrList_ . La structure **ADRENTRY** contient un tableau de valeurs de propriété de destinataire, un d'entre eux est le type du destinataire, ou la propriété **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). Cette structure **ADRLIST** peut être passée à un client à utiliser en tant que paramètre à un appel à [IMessage::ModifyRecipients](imessage-modifyrecipients.md) _lpMods_ .
  
Chaque destinataire de la structure **ADRLIST** peut être soit résolu, ce qui indique qu’une de ses valeurs de propriété est sa propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), ou non, qui indique que la propriété **PR_ENTRYID** est manquante. 
  
Outre **PR_ENTRYID**, destinataires résolus comprennent les propriétés suivantes :
  
- **PR_RECIPIENT_TYPE**
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
En règle générale, les destinataires non résolus incluent uniquement **PR_DISPLAY_NAME** et **PR_RECIPIENT_TYPE**. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

La structure **ADRLIST** qui transmet l’appelant peut être une taille différente de la structure renvoie MAPI. Lorsque vous affectez la mémoire pour la structure **ADRLIST** , allouer la mémoire pour chaque structure [SPropValue](spropvalue.md) séparément. 
  
Utilisez les pointeurs vers les fonctions d’allocation de mémoire MAPI à votre fonction [ABProviderInit](abproviderinit.md) d’allocation de mémoire. Allouer de la mémoire avec la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) pour **ADRLIST** et chaque structure de valeur de propriété dans les structures **ADRENTRY** dans **ADRLIST**. 
  
Si **l’adresse** doit renvoyer une plus grande structure **ADRLIST** , ou si vous avez passé NULL pour _lppAdrList_, **adresse** libère la structure d’origine et alloue un nouveau. **Adresse** également alloue les structures de valeur de propriété supplémentaires dans la structure **ADRLIST** et libère anciens comme il convient. Pour plus d’informations sur la gestion de la mémoire pour les structures **ADRLIST** , voir [Gestion de la mémoire ADRLIST des Structures SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).
  
 **Adresse** renvoie immédiatement si l’indicateur DIALOG_SDI a été défini dans la structure **ADRPARM** dans le paramètre _lpAdrParms_ . 
  
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

