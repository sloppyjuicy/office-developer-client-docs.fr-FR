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
ms.openlocfilehash: f8c129e772870804ef464765b2035a3582317a09
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412981"
---
# <a name="iaddrbookgetsearchpath"></a>IAddrBook::GetSearchPath

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une liste triée d'identificateurs d'entrée des conteneurs à inclure dans le processus de résolution de noms initié par la méthode [IAddrBook:: ResolveName](iaddrbook-resolvename.md) . 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le type des chaînes renvoyées dans le chemin de recherche. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les chaînes renvoyées sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.
    
 _lppSearchPath_
  
> remarquer Pointeur vers un pointeur vers une liste triée d'identificateurs d'entrée de conteneur. **GetSearchPath** stocke la liste ordonnée dans une structure [SRowSet](srowset.md) . S'il n'y a pas de conteneur dans la hiérarchie du carnet d'adresses, zéro est renvoyé dans la structure **SRowSet** . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le chemin de recherche a été correctement récupéré.
    
## <a name="remarks"></a>Remarques

Les clients et les fournisseurs de services appellent la méthode **GetSearchPath** pour obtenir le chemin de recherche utilisé pour résoudre les noms à l'aide de la méthode **ResolveName** . En règle générale, les clients appellent la méthode [IAddrBook:: SetSearchPath](iaddrbook-setsearchpath.md) pour établir un chemin de recherche de conteneur dans le profil avant d'appeler **GetSearchPath** pour le récupérer. Toutefois, l'appel de **SetSearchPath** est facultatif. 
  
Si **SetSearchPath** n'a jamais été appelé, **GetSearchPath** crée un chemin d'accès en utilisant les tables de hiérarchie du carnet d'adresses. Le chemin de recherche par défaut établi par **GetSearchPath** est constitué des conteneurs suivants dans l'ordre suivant: 
  
1. Le premier conteneur avec l'autorisation en lecture/écriture, généralement le carnet d'adresses personnel (PAB).
    
2. Tous les conteneurs dont la propriété **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) est définie sur DT_GLOBAL. Ce paramètre indique que le conteneur détient des destinataires. 
    
3. Conteneur désigné comme valeur par défaut, s'il n'existe pas de conteneur dont l'indicateur DT_GLOBAL est défini dans la propriété **PR_DISPLAY_TYPE** et que le conteneur par défaut diffère du premier conteneur doté de l'autorisation en lecture/écriture. 
    
Si **SetSearchPath** a été appelé, **GetSearchPath** crée un chemin d'accès à l'aide des conteneurs du carnet d'adresses qui ont été stockés dans le profil. **GetSearchPath** valide ce chemin d'accès avant de le renvoyer à l'appelant. 
  
Après le premier appel à **SetSearchPath**, les appels suivants à **SetSearchPath** doivent être utilisés pour modifier le chemin de recherche retourné par **GetSearchPath**. En d'autres termes, le client ou le fournisseur appelant ne reçoit pas le chemin de recherche par défaut après le premier appel à **SetSearchPath**.
  
## <a name="see-also"></a>Voir aussi



[IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

