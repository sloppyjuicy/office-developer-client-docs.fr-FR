---
title: IABContainerResolveNames
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.ResolveNames
api_type:
- COM
ms.assetid: 27474af2-29a2-4cfb-b94f-72eb91562dac
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: fac4978bef94650f85ac3179acd3858602f933ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405813"
---
# <a name="iabcontainerresolvenames"></a>IABContainer::ResolveNames

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Effectue la résolution de noms pour une ou plusieurs entrées de destinataires.
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a>Paramètres

 _lpPropTagArray_
  
> dans Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété décrivant les propriétés à inclure dans la structure [ADRLIST](adrlist.md) renvoyée par le fournisseur. Pour demander le jeu de propriétés par défaut du fournisseur, transmettez la valeur NULL dans le paramètre _lpPropTagArray_ . 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le type du texte dans les chaînes renvoyées. Les indicateurs suivants peuvent être définis:
    
EMS_AB_ADDRESS_LOOKUP
  
> Seules les correspondances d'adresse proxy exactes seront trouvées; les correspondances partielles sont ignorées. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.
    
MAPI_CACHE_ONLY
  
> Seul le carnet d'adresses en mode hors connexion sera utilisé pour la résolution de noms. Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d'ouvrir la liste d'adresses globale (LAG) en mode Exchange mis en cache et d'accéder à une entrée de ce carnet d'adresses à partir du cache sans créer de trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange. 
    
MAPI_UNICODE 
  
> Les propriétés de chaîne retournées sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.
    
 _lpAdrList_
  
> [in, out] En entrée, pointeur vers une structure **ADRLIST** qui contient la liste des destinataires à résoudre. En sortie, pointeur vers une structure **ADRLIST** qui contient les noms résolus. 
    
 _lpFlagList_
  
> [in, out] Pointeur vers un tableau d'indicateurs, chaque indicateur correspondant à une structure [ADRENTRY](adrentry.md) dans le paramètre _lpAdrList_ , qui fournit l'état de l'opération de résolution de noms pour le destinataire. Les indicateurs dans le paramètre _lpFlagList_ sont dans le même ordre que les entrées dans _lpAdrList_. Les indicateurs suivants peuvent être définis:
    
MAPI_AMBIGUOUS 
  
> Le destinataire correspondant a été résolu, mais pas à un identificateur d'entrée unique. Les autres conteneurs ne doivent pas essayer de résoudre ce destinataire. 
    
MAPI_RESOLVED 
  
> Le destinataire correspondant a été résolu en un identificateur d'entrée unique. Les autres conteneurs ne doivent pas essayer de résoudre ce destinataire. 
    
MAPI_UNRESOLVED 
  
> L'entrée correspondante n'a pas été résolue. D'autres conteneurs doivent essayer de résoudre ce destinataire.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le processus de résolution de noms a réussi.
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de carnet d'adresses ne prend pas en charge la résolution de noms en bloc à l'aide de cette méthode.
    
## <a name="remarks"></a>Remarques

La méthode **ResolveNames** tente de faire correspondre les destinataires non résolus du tableau d'entrées du paramètre _lpAdrList_ aux destinataires de ce conteneur de carnet d'adresses. Un destinataire non résolu dispose généralement uniquement de la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) et éventuellement d'autres propriétés. Un destinataire non résolu ne dispose pas de la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) et son indicateur correspondant dans le paramètre _lpFlagList_ est défini sur MAPI_UNRESOLVED. À l'inverse, un destinataire résolu dispose toujours au moins de la propriété **PR_ENTRYID** , ainsi que d'autres propriétés telles que **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**et **PR_ADDRTYPE** ([ PidTagAddressType](pidtagaddresstype-canonical-property.md)).
  
La résolution de noms démarre généralement lorsqu'un client appelle la méthode [IAddrBook:: ResolveName](iaddrbook-resolvename.md) . Outlook MAPI répond en appelant la méthode **ResolveNames** de chaque conteneur de carnet d'adresses inclus dans le chemin de recherche de carnet d'adresses, spécifié par la propriété **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)). Les entrées du paramètre _lpAdrList_ incluent les destinataires déjà résolus car il s'agit de conteneurs pour lesquels MAPI a déjà appelé **ResolveNames**, car les entrées apparaissent plus tôt dans le chemin de recherche. 
  
Chaque conteneur tente de résoudre les entrées non résolues en faisant correspondre le nom d'affichage du destinataire avec le nom d'affichage de l'une de ses entrées. Lorsqu'une correspondance unique est trouvée, **ResolveNames** ajoute la propriété **PR_ENTRYID** et d'autres propriétés incluses dans le paramètre _lpPropTagArray_ à l'entrée correspondante dans la structure **ADRLIST** sortante. **ResolveNames** définit ensuite l'entrée dans le paramètre _lpFlagList_ sur MAPI_RESOLVED. L'identificateur d'entrée stocké dans la propriété **PR_ENTRYID** peut être court ou long terme. 
  
Une fois que tous les conteneurs dans le chemin de recherche ont tenté le processus de résolution de noms, MAPI ouvre une boîte de dialogue, si possible, pour inviter l'utilisateur à trouver de l'aide pour résoudre les conflits restants. 
  
Les clients peuvent également utiliser la structure **ADRLIST** renvoyée dans les appels à la méthode [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) . 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous n'êtes pas obligé de prendre en charge la résolution de nom avec la méthode **ResolveNames** . Au lieu de cela, vous pouvez également le prendre en charge à l'aide de la restriction de propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)). Si vous décidez de reposer sur la restriction **PR_ANR** pour la résolution de noms, vous pouvez renvoyer MAPI_E_NO_SUPPORT. For more information, see [L'impl�mentation de la r�solution de noms](implementing-name-resolution.md).
  
Définissez l'entrée d'indicateur d'un destinataire dans le paramètre _lpFlagList_ sur MAPI_UNRESOLVED si le destinataire ne correspond à aucun des destinataires du conteneur. 
  
Lorsqu'un destinataire correspond à plusieurs destinataires, définissez son indicateur sur MAPI_AMBIGUOUS et ne modifiez pas sa structure **ADRENTRY** . 
  
MAPI requiert certaines propriétés pour les destinataires inclus dans la liste des destinataires d'un message. Vous pouvez les inclure dans la structure **ADRENTRY** dans le cadre du processus de résolution de noms ou attendre MAPI pour les demander avec des appels à [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) et [IMAPISupport:: ExpandRecips](imapisupport-expandrecips.md) methods. Vous pouvez éliminer ces appels supplémentaires et améliorer les performances en incluant les propriétés suivantes dans les structures **ADRENTRY** de tous les destinataires résolus: 
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Si certaines propriétés du paramètre _lpPropTagArray_ ne sont pas disponibles, en général parce que l'entrée de conteneur ne prend pas en charge les propriétés et qu'elles ne sont pas incluses dans le membre **ADRENTRY** du destinataire dans la structure **ADRLIST** , Définissez le type de propriété de chaque propriété unavailable sur PT_ERROR. 
  
Ne supprimez pas les propriétés de la structure **ADRENTRY** d'un destinataire résolu. 
  
Si vous devez remplacer au lieu de modifier une structure **ADRENTRY** , libérez d'abord la structure **ADRENTRY** d'origine en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) , puis allouez la structure de **ADRENTRY** de remplacement avec [ MAPIAllocateBuffer](mapiallocatebuffer.md).
  
## <a name="see-also"></a>Voir aussi



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPISupport::ExpandRecips](imapisupport-expandrecips.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[Propriété canonique PidTagAnr](pidtaganr-canonical-property.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

