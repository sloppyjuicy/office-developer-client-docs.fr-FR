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
ms.openlocfilehash: 81f35f659342d6258d60f40b12bd0a3ac2dc20b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588474"
---
# <a name="iabcontainerresolvenames"></a>IABContainer::ResolveNames

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Effectue la résolution de noms pour une ou plusieurs entrées de destinataire.
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a>Param�tres

 _lpPropTagArray_
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriétés décrivant les propriétés à inclure dans la structure [ADRLIST](adrlist.md) retournée par le fournisseur. Pour demander le jeu de propriétés par défaut du fournisseur, passez la valeur NULL dans le paramètre _lpPropTagArray_ . 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type du texte dans les chaînes retournées. Les indicateurs suivants peuvent être définis :
    
EMS_AB_ADDRESS_LOOKUP
  
> Vous trouverez les correspondances d’adresse proxy exacte uniquement ; correspondances partielles sont ignorés. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.
    
MAPI_CACHE_ONLY
  
> Uniquement le carnet d’adresses en mode hors connexion permet de résoudre les noms. Par exemple, vous pouvez utiliser cet indicateur pour activer une application cliente ouvrir la liste d’adresses globale (LAG) en mode exchange mis en cache et accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer le trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange. 
    
MAPI_UNICODE 
  
> Les propriétés de la chaîne retournée sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _lpAdrList_
  
> [entrée, sortie] À l’entrée, un pointeur vers une structure **ADRLIST** qui contient la liste des destinataires à résoudre. Dans la sortie, un pointeur vers une structure **ADRLIST** qui contient les noms résolus. 
    
 _lpFlagList_
  
> [entrée, sortie] Un pointeur vers un tableau d’indicateurs, chaque indicateur correspondant à une structure [ADRENTRY](adrentry.md) dans le paramètre _lpAdrList_ , qui fournit l’état de l’opération de résolution de nom pour le destinataire. Les indicateurs dans le paramètre _lpFlagList_ sont dans le même ordre que les entrées dans _lpAdrList_. Les indicateurs suivants peuvent être définis :
    
MAPI_AMBIGUOUS 
  
> Le destinataire a été résolu, mais pas à un identificateur d’entrée unique. Autres conteneurs ne doivent pas essayer de résoudre ce destinataire. 
    
MAPI_RESOLVED 
  
> Le destinataire a été résolu à un identificateur d’entrée unique. Autres conteneurs ne doivent pas essayer de résoudre ce destinataire. 
    
MAPI_UNRESOLVED 
  
> L’entrée correspondante n’a pas été résolue. Autres conteneurs doivent essayer de résoudre ce destinataire.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le processus de résolution de nom a réussi.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de carnet d’adresses ne gère pas la résolution de noms en bloc à l’aide de cette méthode.
    
## <a name="remarks"></a>Remarques

La méthode **ResolveNames** tente de faire correspondre les destinataires du tableau des entrées dans le paramètre _lpAdrList_ aux destinataires de ce conteneur de carnet d’adresses. Généralement, un destinataire non résolu a uniquement la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) et éventuellement quelques autres propriétés. Un destinataire non résolu n’a pas la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) et son correspondante dans le paramètre _lpFlagList_ est défini à MAPI_UNRESOLVED. Inversement, un destinataire résolu a toujours au moins la propriété **PR_ENTRYID** ainsi que plusieurs autres propriétés telles que **TYPEADR_PR** ([ , **PR_DISPLAY_NAME**et **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) PidTagAddressType](pidtagaddresstype-canonical-property.md)).
  
Résolution de noms commence généralement lorsqu’un client appelle la méthode [IAddrBook::ResolveName](iaddrbook-resolvename.md) . Outlook MAPI répond en appelant la méthode **ResolveNames** de chaque conteneur de carnet d’adresses incluse dans le chemin de recherche de livre adresse, spécifié par la propriété **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)). Les entrées dans le paramètre _lpAdrList_ les destinataires déjà résolus car ils sont dans des conteneurs dont MAPI a déjà appelé **ResolveNames**, étant donné que les entrées apparaissent plus haut dans le chemin de recherche. 
  
Chaque conteneur essaie de résoudre les entrées non résolues par correspondant au nom d’affichage du destinataire dont le nom complet de l’un de ses entrées. Lorsqu’une correspondance unique est trouvée, **ResolveNames** ajoute la propriété **PR_ENTRYID** et autres propriétés qui sont incluses dans le paramètre _lpPropTagArray_ à l’entrée correspondante dans la structure **ADRLIST** sortante. **ResolveNames** définit ensuite l’entrée dans le paramètre _lpFlagList_ pour MAPI_RESOLVED. L’identificateur d’entrée stockée dans la propriété **PR_ENTRYID** peut être à court terme ou à long terme. 
  
Après tout des conteneurs de la recherche de chemin d’accès tenté le processus de résolution de noms, MAPI ouvre une boîte de dialogue, dans la mesure du possible, pour inviter l’utilisateur à l’aide pour résoudre les conflits restants. 
  
Les clients peuvent également utiliser la structure **ADRLIST** retournée dans les appels à la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Vous ne sont pas requis pour prendre en charge la résolution de noms avec la méthode **ResolveNames** . Au lieu de cela, ou en outre, vous pouvez en charge avec la restriction de propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)). Si vous décidez s’appuient sur la restriction de **PR_ANR** pour la résolution de noms, vous pouvez retourner MAPI_E_NO_SUPPORT. For more information, see [L'impl�mentation de la r�solution de noms](implementing-name-resolution.md).
  
Définissez l’entrée indicateur d’un destinataire dans le paramètre _lpFlagList_ pour MAPI_UNRESOLVED si le destinataire ne correspond pas à un des destinataires du conteneur. 
  
Lorsqu’un destinataire correspond à plusieurs destinataires, affectez à son indicateur MAPI_AMBIGUOUS et ne modifiez pas la structure **ADRENTRY** . 
  
MAPI nécessite certaines propriétés pour les destinataires qui sont inclus dans la liste des destinataires d’un message. Vous pouvez les inclure dans la structure **ADRENTRY** dans le cadre du processus de résolution de nom ou attendre MAPI demander les avec les appels aux méthodes [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) et [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) . Vous pouvez éliminer ces appels supplémentaires et améliorer les performances en y compris les propriétés suivantes dans les structures **ADRENTRY** de tous les destinataires résolus : 
  
- **TYPEADR_PR**
    
- **PR_DISPLAY_NAME**
    
- **ADRESSE_EMAIL_PR**
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **Clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Si certaines des propriétés dans le paramètre _lpPropTagArray_ ne sont pas disponibles, en général car l’entrée de conteneur ne gère pas les propriétés et qu’ils ne figurent pas dans le membre **ADRENTRY** du destinataire dans la structure **ADRLIST** : définir le type de propriété de chaque propriété non disponible PT_ERROR. 
  
Ne supprimez pas toutes les propriétés de structure de **ADRENTRY** d’un destinataire résolu. 
  
Si vous devez remplacer plutôt que de modifier une structure **ADRENTRY** , libérer la structure **ADRENTRY** d’origine en appelant d’abord la fonction [MAPIFreeBuffer](mapifreebuffer.md) , puis allouer le remplacement structure **ADRENTRY** avec [ MAPIAllocateBuffer](mapiallocatebuffer.md).
  
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

