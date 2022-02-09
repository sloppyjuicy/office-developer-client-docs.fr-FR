---
title: IAddrBookResolveName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.ResolveName
api_type:
- COM
ms.assetid: a7823c16-efda-45c2-b931-3e1fbc823b0b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c2a5ddd75ee0b817ef780518a7ee7c9a9896bc00
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462016"
---
# <a name="iaddrbookresolvename"></a>IAddrBook::ResolveName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Effectue la résolution de noms, en attribuant des identificateurs d’entrée aux destinataires d’une liste de destinataires.
  
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
  
> [in] Poignée vers la fenêtre parente d’une boîte de dialogue qui s’affiche, si elle est spécifiée, pour inciter l’utilisateur à résoudre l’ambiguïté.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôlent différents aspects du processus de résolution. Les indicateurs suivants peuvent être définies :
    
AB_UNICODEUI
  
> Indique que  _lpszNewEntryTitle est_ une chaîne UNICODE. 
    
MAPI_CACHE_ONLY
  
> Utilisez uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms. Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d’ouvrir la liste d’adresses globale (LAL) en mode Exchange mis en cache et d’accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer de trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le Exchange de carnet d’adresses.
    
MAPI_DIALOG 
  
> Affiche une boîte de dialogue qui invite l’utilisateur à fournir des informations supplémentaires sur la résolution de noms. Si cet indicateur n’est pas définie, aucune boîte de dialogue n’est affichée. 
    
MAPI_UNICODE 
  
> Indique que les propriétés renvoyées dans la liste d’adresses doivent être de type PT_UNICODE au lieu de PT_STRING8. 
    
 _lpszNewEntryTitle_
  
> [in] Pointeur vers du texte pour le titre du contrôle dans la boîte de dialogue qui invite l’utilisateur à entrer un destinataire. Le titre varie en fonction du type de destinataire. Le  _paramètre lpszNewEntryTitle_ peut être NULL. 
    
 _lpAdrList_
  
> [in-out] Pointeur vers une structure [ADRLIST](adrlist.md) qui contient la liste des noms de destinataires à résoudre. Cette structure **ADRLIST** peut être créée par la [méthode IAddrBook::Address](iaddrbook-address.md) . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le processus de résolution de noms a réussi.
    
MAPI_E_AMBIGUOUS_RECIP 
  
> Au moins un destinataire dans le _paramètre lpAdrList_ correspond à plusieurs entrées dans le carnet d’adresses. En règle générale, cette valeur est renvoyée lorsque l’MAPI_DIALOG est définie, ce qui interdit l’affichage d’une boîte de dialogue. 
    
MAPI_E_NOT_FOUND 
  
> Au moins un destinataire dans le _paramètre lpAdrList_ ne peut pas être résolu. En règle générale, cette valeur est renvoyée lorsque l’MAPI_DIALOG est définie, ce qui interdit l’affichage d’une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Les clients et les fournisseurs de services appellent **la méthode ResolveName** pour lancer le processus de résolution de noms. Une entrée non résolue est une entrée qui n’a pas encore d’identificateur d’entrée **PR_ENTRYID propriété (**[PidTagEntryId](pidtagentryid-canonical-property.md)).
  
 **ResolveName** suit le processus suivant pour chaque entrée non résolue dans la liste d’adresses transmise dans _le paramètre lpAdrList_ . 
  
1. Si le type d’adresse du destinataire respecte le format d’une adresse SMTP (_nom_@  d’affichage _domain.top-niveau-domaine_), **ResolveName** lui attribue un identificateur d’entrée unique. 
    
2. Pour chaque conteneur de la **propriété PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)), **ResolveName** appelle la méthode [IABContainer::ResolveNames](iabcontainer-resolvenames.md) . **ResolveNames tente de** faire correspondre le nom complet de chaque destinataire non résolu avec un nom complet qui appartient à l’une de ses entrées. 
    
3. Si un conteneur ne prend pas en charge **ResolveNames**, **ResolveName** limite la table des matières du conteneur à l’aide d’une restriction de propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)). Cette restriction entraîne le conteneur à effectuer un type de recherche de « meilleure estimation » pour localiser un destinataire correspondant. Tous les conteneurs doivent prendre en charge **PR_ANR** restriction de propriété. 
    
4. Lorsqu’un conteneur renvoie un destinataire qui correspond à plusieurs noms, **ResolveName** affiche une boîte de dialogue si l’indicateur MAPI_DIALOG est définie, ce qui permet à l’utilisateur de sélectionner le nom correct. 
    
5. Si tous les conteneurs de la **propriété PR_AB_SEARCH_PATH** ont été appelés et qu’aucune correspondance n’a été trouvée, le destinataire reste non résolu. 
    
Si un ou plusieurs destinataires ne sont pas résolus, **ResolveName** renvoie MAPI_E_NOT_FOUND. Si un ou plusieurs destinataires avaient une résolution ambiguë qui n’a pas pu être résolue avec une boîte de dialogue ou parce que l’indicateur MAPI_DIALOG n’a pas été définie, **ResolveName** renvoie MAPI_E_AMBIGUOUS_RECIP. Lorsque certains destinataires sont ambigus et que d’autres ne peuvent pas être résolus, **ResolveName** peut renvoyer l’une ou l’autre des valeurs d’erreur. 
  
Si un nom ne peut pas être résolu, le client peut créer une adresse unique avec un identificateur d’adresse et d’entrée spécialement mis en forme. Pour plus d’informations sur le format des identificateurs d’entrée uniques, voir [Identificateurs d’entrée uniques](one-off-entry-identifiers.md). Pour plus d’informations sur le format des adresses one-off, voir [Adresses one-off](one-off-addresses.md).
  
MAPI prend en charge les chaînes de caractères Unicode pour **ADRLIST** et les nouveaux paramètres de titre d’entrée **pour ResolveName** ; Si vous définissez l’MAPI_UNICODE, les propriétés suivantes sont renvoyées en tant que PT_UNICODE dans les structures [ADRENTRY](adrentry.md) : 
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Toutefois, **la propriété PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) est toujours renvoyée en tant que type PT_STRING8.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI utilise la **méthode ResolveName** pour résoudre une adresse one-off avant de l’ajouter à un message.  <br/> |
|MAPIABFunctions.cpp  <br/> |AddRecipient  <br/> |MFCMAPI utilise la **méthode ResolveName** pour rechercher une entrée de carnet d’adresses par nom d’affichage.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

