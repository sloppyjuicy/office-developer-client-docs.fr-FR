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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 1f09c88d9bd6720720e2d30ac24fa4a19aed5538
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567229"
---
# <a name="iaddrbookresolvename"></a>IAddrBook::ResolveName

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Effectue la résolution de noms, affectation d’identificateurs d’entrée aux destinataires dans une liste de destinataires.
  
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
  
> [in] Un handle vers la fenêtre parent d’une boîte de dialogue qui s’affiche, si spécifié, pour inviter l’utilisateur à résoudre l’ambiguïté.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôlent les différents aspects du processus de résolution. Les indicateurs suivants peuvent être définis :
    
AB_UNICODEUI
  
> Indique que _lpszNewEntryTitle_ est une chaîne UNICODE. 
    
MAPI_CACHE_ONLY
  
> Utilisez uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms. Par exemple, vous pouvez utiliser cet indicateur pour autoriser une application cliente ouvrir la liste d’adresses globale (LAG) en mode exchange mis en cache et accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer le trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.
    
MAPI_DIALOG 
  
> Affiche une boîte de dialogue pour inviter l’utilisateur pour les informations de résolution de nom supplémentaire. Si cet indicateur n’est pas défini, aucune boîte de dialogue ne s’affiche. 
    
MAPI_UNICODE 
  
> Indique que les propriétés renvoyées dans la liste d’adresses doivent être de type PT_UNICODE au lieu de PT_STRING8. 
    
 _lpszNewEntryTitle_
  
> [in] Pointeur vers le texte du titre du contrôle dans la boîte de dialogue qui invite l’utilisateur à entrer un destinataire. Le titre varie selon le type de destinataire. Le paramètre _lpszNewEntryTitle_ peut être NULL. 
    
 _lpAdrList_
  
> [-out] Pointeur vers une structure [ADRLIST](adrlist.md) qui contient la liste des noms des destinataires à résoudre. Cette structure **ADRLIST** peut être créée par la méthode [IAddrBook::Address](iaddrbook-address.md) . 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le processus de résolution de nom a réussi.
    
MAPI_E_AMBIGUOUS_RECIP 
  
> Au moins un destinataire dans le paramètre _lpAdrList_ correspondant plus d’une entrée dans le carnet d’adresses. En règle générale, cette valeur est renvoyée lorsque la valeur de l’indicateur MAPI_DIALOG, interdisant l’affichage d’une boîte de dialogue. 
    
MAPI_E_NOT_FOUND 
  
> Au moins un destinataire dans le paramètre _lpAdrList_ ne peut pas être résolu. En règle générale, cette valeur est renvoyée lorsque la valeur de l’indicateur MAPI_DIALOG, interdisant l’affichage d’une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Clients et fournisseurs de services appellent la méthode **ResolveName** pour lancer le processus de résolution de nom. Une entrée non résolue est une entrée qui n’a pas encore un identificateur d’entrée ou de la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
 **ResolveName** passe par le processus suivant pour chaque entrée dans la liste d’adresses passée dans le paramètre _lpAdrList_ non résolue. 
  
1. Si le type d’adresse du destinataire respecte le format d’adresse SMTP ( _displayname_@ _domaine de niveau domain.top_), **ResolveName** lui attribue un identificateur d’entrée unique. 
    
2. Pour chaque conteneur dans la propriété **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)), **ResolveName** appelle la méthode [IABContainer::ResolveNames](iabcontainer-resolvenames.md) . **ResolveNames** tente de faire correspondre le nom complet de chaque destinataire non résolu avec un nom d’affichage qui appartienne à l’un de ses entrées. 
    
3. Si un conteneur ne prend pas en charge **ResolveNames**, **ResolveName** limite la table des matières du conteneur à l’aide d’une restriction de propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)). Cette restriction provoque le conteneur exécuter un type de recherche pour localiser un destinataire correspondant « mieux deviner ». Tous les conteneurs doivent prendre en charge la restriction de propriété **PR_ANR** . 
    
4. Lorsqu’un conteneur renvoie un destinataire qui correspond à plusieurs noms, **ResolveName** affiche une boîte de dialogue si l’indicateur MAPI_DIALOG est défini, ce qui permet à l’utilisateur de sélectionner le nom correct. 
    
5. Si tous les conteneurs dans la propriété **PR_AB_SEARCH_PATH** ont été appelées et si aucune correspondance n’a été trouvée, le destinataire reste non résolu. 
    
Si un ou plusieurs destinataires résolues, **ResolveName** renvoie MAPI_E_NOT_FOUND. Si un ou plusieurs destinataires AMBIGUE résolution qui n’a pas pu être résolue avec une boîte de dialogue, ou parce que l’indicateur MAPI_DIALOG n’a pas été défini, **ResolveName** renvoie MAPI_E_AMBIGUOUS_RECIP. Lorsque des destinataires sont ambigus et certaines ne peut pas être résolu, **ResolveName** peut renvoyer une valeur d’erreur. 
  
Si un nom ne peut pas être résolu, le client peut créer une adresse unique ayant une adresse spécialement mise en forme et l’identificateur d’entrée. Pour plus d’informations sur le format des identificateurs d’entrée unique, voir [Identificateurs uniques d’entrée](one-off-entry-identifiers.md). Pour plus d’informations sur le format des adresses uniques, voir [Adresses uniques](one-off-addresses.md).
  
MAPI prend en charge les chaînes de caractères Unicode pour les **ADRLIST** et les nouveaux paramètres de titre de l’entrée à **ResolveName**; Si vous définissez l’indicateur MAPI_UNICODE, les propriétés suivantes sont renvoyées sous forme de type PT_UNICODE dans les structures [ADRENTRY](adrentry.md) : 
  
- **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Toutefois, la propriété **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) est toujours renvoyée comme type PT_STRING8.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI utilise la méthode **ResolveName** pour résoudre une adresse unique avant son ajout à un message.  <br/> |
|MAPIABFunctions.cpp  <br/> |Ajouter destinataire  <br/> |MFCMAPI utilise la méthode **ResolveName** pour rechercher une entrée de carnet d’adresses par nom complet.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

