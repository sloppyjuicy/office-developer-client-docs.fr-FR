---
title: IAddrBookResolveName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.ResolveName
api_type:
- COM
ms.assetid: a7823c16-efda-45c2-b931-3e1fbc823b0b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8a6a73153b857078cb37d94a634a6b0215a0a8c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287006"
---
# <a name="iaddrbookresolvename"></a>IAddrBook::ResolveName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Effectue une résolution de noms, en affectant des identificateurs d'entrée à des destinataires dans une liste de destinataires.
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> dans Handle de la fenêtre parent d'une boîte de dialogue qui s'affiche, s'il est spécifié, pour inviter l'utilisateur à résoudre une ambiguïté.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôlent différents aspects du processus de résolution. Les indicateurs suivants peuvent être définis:
    
AB_UNICODEUI
  
> Indique que _lpszNewEntryTitle_ est une chaîne Unicode. 
    
MAPI_CACHE_ONLY
  
> Utilisez uniquement le carnet d'adresses en mode hors connexion pour effectuer la résolution de noms. Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d'ouvrir la liste d'adresses globale (LAG) en mode Exchange mis en cache et d'accéder à une entrée de ce carnet d'adresses à partir du cache sans créer de trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.
    
MAPI_DIALOG 
  
> Affiche une boîte de dialogue pour inviter l'utilisateur à fournir des informations de résolution de noms supplémentaires. Si cet indicateur n'est pas défini, aucune boîte de dialogue ne s'affiche. 
    
MAPI_UNICODE 
  
> Indique que les propriétés retournées dans la liste d'adresses doivent être de type PT_UNICODE au lieu de PT_STRING8. 
    
 _lpszNewEntryTitle_
  
> dans Pointeur vers le texte du titre du contrôle dans la boîte de dialogue invitant l'utilisateur à entrer un destinataire. Le titre varie en fonction du type de destinataire. Le paramètre _lpszNewEntryTitle_ peut être null. 
    
 _lpAdrList_
  
> [in-out] Pointeur vers une structure [ADRLIST](adrlist.md) qui contient la liste des noms des destinataires à résoudre. Cette structure **ADRLIST** peut être créée par la méthode [IAddrBook:: Address](iaddrbook-address.md) . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le processus de résolution de noms a réussi.
    
MAPI_E_AMBIGUOUS_RECIP 
  
> Au moins un destinataire dans le paramètre _lpAdrList_ correspond à plusieurs entrées dans le carnet d'adresses. En règle générale, cette valeur est renvoyée lorsque l'indicateur MAPI_DIALOG est défini, ce qui interdit l'affichage d'une boîte de dialogue. 
    
MAPI_E_NOT_FOUND 
  
> Au moins un destinataire dans le paramètre _lpAdrList_ ne peut pas être résolu. En règle générale, cette valeur est renvoyée lorsque l'indicateur MAPI_DIALOG est défini, ce qui interdit l'affichage d'une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Les clients et les fournisseurs de services appellent la méthode **ResolveName** pour lancer le processus de résolution de noms. Une entrée non résolue est une entrée qui n'a pas encore d'identificateur d'entrée ou de propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
 **ResolveName** passe en revue le processus suivant pour chaque entrée non résolue dans la liste d'adresses passée dans le paramètre _lpAdrList_ . 
  
1. Si le type d'adresse du destinataire adhère au format d'une adresse SMTP (domaine _DisplayName_@ _. domaine de niveau supérieur_), **ResolveName** lui affecte un identificateur d'entrée unique. 
    
2. Pour chaque conteneur dans la propriété **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)), **ResolveName** appelle la méthode [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) . **ResolveNames** tente de faire correspondre le nom d'affichage de chaque destinataire non résolu à un nom complet qui appartient à l'une de ses entrées. 
    
3. Si un conteneur ne prend pas en charge **ResolveNames**, **ResolveName** limite la table des matières du conteneur à l'aide d'une restriction de propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)). Cette restriction fait en sorte que le conteneur effectue un type de recherche «meilleure estimation» pour localiser un destinataire correspondant. Tous les conteneurs doivent prendre en charge la restriction de propriété **PR_ANR** . 
    
4. Lorsqu'un conteneur renvoie un destinataire qui correspond à plusieurs noms, **ResolveName** affiche une boîte de dialogue si l'indicateur MAPI_DIALOG est défini, ce qui permet à l'utilisateur de sélectionner le nom correct. 
    
5. Si tous les conteneurs de la propriété **PR_AB_SEARCH_PATH** ont été appelés et qu'aucune correspondance n'a été trouvée, le destinataire reste non résolu. 
    
Si un ou plusieurs destinataires ne sont pas résolus, **ResolveName** renvoie MAPI_E_NOT_FOUND. Si un ou plusieurs destinataires ont une résolution ambiguë qui n'a pas pu être résolue à l'aide d'une boîte de dialogue ou parce que l'indicateur MAPI_DIALOG n'a pas été défini, **ResolveName** renvoie MAPI_E_AMBIGUOUS_RECIP. Lorsqu'une partie des destinataires est ambiguë et qu'une partie ne peut pas être résolue, **ResolveName** peut renvoyer l'une des valeurs d'erreur. 
  
Si un nom ne peut pas être résolu, le client peut créer une adresse unique ayant une adresse et un identificateur d'entrée spécialement mis en forme. Pour plus d'informations sur le format des identificateurs d'entrée uniques, consultez la rubrique identificateurs d' [entrée uniques](one-off-entry-identifiers.md). Pour plus d'informations sur le format des adresses ponctuelles, consultez la rubrique [adresses ponctuelles](one-off-addresses.md).
  
MAPI prend en charge les chaînes de caractères Unicode pour le **ADRLIST** et les nouveaux paramètres de titre d'entrée pour **ResolveName**; Si vous définissez l'indicateur MAPI_UNICODE, les propriétés suivantes sont renvoyées en tant que type PT_UNICODE dans les structures [ADRENTRY](adrentry.md) : 
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Toutefois, la propriété **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) est toujours renvoyée en tant que type PT_STRING8.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIABFunctions. cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI utilise la méthode **ResolveName** pour résoudre une adresse ponctuelle avant de l'ajouter à un message.  <br/> |
|MAPIABFunctions. cpp  <br/> |AddRecipient  <br/> |MFCMAPI utilise la méthode **ResolveName** pour rechercher une entrée de carnet d'adresses par son nom complet.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

