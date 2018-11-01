---
title: IAddrBookGetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetSearchPath
api_type:
- COM
ms.assetid: 43b51a66-71fa-4e10-93e4-d533b48af4de
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7bf69e560142ab282d6545389e02766389e4d018
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580697"
---
# <a name="iaddrbookgetsearchpath"></a>IAddrBook::GetSearchPath

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une liste triée des identificateurs d’entrée des conteneurs à inclure dans le processus de résolution de noms initié par la méthode [IAddrBook::ResolveName](iaddrbook-resolvename.md) . 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type des chaînes renvoyées dans le chemin de recherche. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes retournées sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _lppSearchPath_
  
> [out] Pointeur vers un pointeur vers une liste triée des identificateurs d’entrée de conteneur. **GetSearchPath** stocke la liste dans une structure [SRowSet](srowset.md) . S’il n’y a aucun conteneur dans la hiérarchie de carnets d’adresses, zéro est retournée dans la structure **SRowSet** . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le chemin de recherche a été récupéré correctement.
    
## <a name="remarks"></a>Remarques

Clients et fournisseurs de services appellent la méthode **GetSearchPath** pour obtenir le chemin de recherche qui est utilisé pour résoudre les noms avec la méthode **ResolveName** . En règle générale, les clients appellent la méthode de [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) pour établir un chemin de recherche du conteneur dans le profil avant d’appeler **GetSearchPath** pour récupérer. Toutefois, l’appel de **SetSearchPath** est facultatif. 
  
Si **SetSearchPath** n’a jamais été appelée, **GetSearchPath** génère un chemin d’accès en passant par l’adresse de tables de hiérarchie du livre. Le chemin de recherche par défaut ouverte par **GetSearchPath** se compose des conteneurs suivants dans l’ordre suivant : 
  
1. Le premier conteneur avec l’autorisation de lecture/écriture, généralement le carnet d’adresses personnel (CAP).
    
2. Chaque conteneur dont la propriété **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) la valeur DT_GLOBAL. Ce paramètre indique que le conteneur contient des destinataires. 
    
3. Le conteneur désigné en tant que la valeur par défaut, s’il n’existe aucun conteneur dont l’indicateur DT_GLOBAL dans leur propriété **PR_DISPLAY_TYPE** et le conteneur par défaut diffère du premier conteneur disposant d’une autorisation en lecture-écriture. 
    
Si **SetSearchPath** a été appelée, **GetSearchPath** génère un chemin d’accès en utilisant les conteneurs du carnet d’adresses qui ont été stockées dans le profil. **GetSearchPath** valide ce chemin d’accès avant qu’il renvoie à l’appelant. 
  
Après le premier appel à **SetSearchPath**, les appels suivants de **SetSearchPath** permet de modifier le chemin d’accès de la recherche renvoyé par **GetSearchPath**. En d’autres termes, le client ou le fournisseur appelant ne reçoit pas le chemin d’accès de la recherche par défaut après le premier appel à **SetSearchPath**.
  
## <a name="see-also"></a>Voir aussi



[IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

