---
title: LAUNCHWIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.LAUNCHWIZARDENTRY
api_type:
- COM
ms.assetid: 5778dffa-f01b-46b3-9c19-862793740918
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ed35eabe27223d8c2af6be0a30e6ec678c0dfc8a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584191"
---
# <a name="launchwizardentry"></a>LAUNCHWIZARDENTRY

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction qui démarre l’application De l’Assistant Profil dans le but d’ajouter un ou plusieurs services de message à un profil. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiwz.h  <br/> |
|Fonction définie implémentée par :  <br/> |MAPI  <br/> |
|Fonction définie appelée par :  <br/> |Applications clientes  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a>Paramètres

 _hParentWnd_
  
> [in] Handle vers la fenêtre parente de l’appelant. Si l’appelant n’a pas de fenêtre parent, le  _paramètre hParentWnd_ doit être NULL. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs indiquant les options de l’Assistant Profil. Les indicateurs suivants peuvent être définies :
    
MAPI_PW_ADD_SERVICE_ONLY 
  
> L’Assistant Profil consiste à ajouter uniquement les services de message répertoriés via le paramètre  _lppszServiceNameToAdd_ et à ne pas afficher sa page pour la sélection des services de message. 
    
MAPI_PW_FIRST_PROFILE 
  
> Le profil à créer est le premier pour cette station de travail. 
    
MAPI_PW_HIDE_SERVICES_LIST 
  
> La page de l’Assistant Profil pour la sélection des services de message ne doit pas s’afficher. 
    
MAPI_PW_LAUNCHED_BY_CONFIG 
  
> L’Assistant Profil a été lancé par l’application de configuration du Panneau de configuration. 
    
MAPI_PW_PROVIDER_UI_ONLY 
  
> Seules les boîtes de dialogue de configuration des fournisseurs de services doivent être affichées et les pages de l’Assistant Profil ne doivent pas apparaître. Cet indicateur ne peut être définie que si l’MAPI_PW_ADD_SERVICE_ONLY est définie. 
    
 _lppszServiceNameToAdd_
  
> [in] Pointeur vers un tableau de chaînes qui contient les noms des services de message à ajouter au profil. Le tableau doit se terminer par une valeur NULL. 
    
 _cbBufferMax_
  
> [in] Taille de la mémoire tampon pointée par _le paramètre lpszNewProfileName._ 
    
 _lpszNewProfileName_
  
> [out] Pointeur vers une mémoire tampon de chaînes où la fonction basée sur **LAUNCHWIZARDENTRY** renvoie le nom du profil créé. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_CALL_FAILED 
  
> Une erreur d’origine inattendue ou inconnue a empêché l’exécution de l’opération. Les possibilités incluent l’échec de l’initialisation du sous-système MAPI pour l’Assistant Profil, l’impossibilité d’accéder au profil par défaut et un retour d’erreur à partir de la boîte de dialogue.
    
## <a name="remarks"></a>Remarques

L’implémentation MAPI du prototype de fonction **LAUNCHWIZARDENTRY** est le point d’entrée dans l’application de l’Assistant Profil MAPI. MAPI nomme ce point d’entrée **LaunchWizard**. 
  
Lorsque l MAPI_PW_ADD_SERVICE_ONLY est définie dans le  _paramètre ulFlags,_ les règles suivantes s’appliquent : 
  
- L MAPI_PW_LAUNCHED_BY_CONFIG empêche l’affichage de la page d’accueil. 
    
- Les indicateurs MAPI_PW_HIDE_SERVICES_LIST et MAPI_PW_PROVIDER_UI_ONLY ne sont utiles qu’en l’absence de profil par défaut. Dans ce cas, ces indicateurs déterminent la page de l’Assistant Profil à afficher. 
    
- S’il existe un profil par défaut, aucune des pages de l’Assistant Profil ne doit être affichée. 
    
- S’il existe un profil par défaut, un seul service de message est répertorié via le paramètre  _lppszServiceNameToAdd_ et que ce service de message figure déjà dans le profil par défaut, l’Assistant Profil renvoie S_OK sans rien ajouter au profil. 
    
Pour chaque service de message à ajouter au profil, l’Assistant Profil appelle la fonction de point d’entrée du service basée sur le prototype [MSGSERVICEENTRY.](msgserviceentry.md) Pour chaque fournisseur de services sélectionné dans un service de messagerie à ajouter au profil, l’Assistant Profil appelle la fonction de point d’entrée du fournisseur basée sur le prototype [WIZARDENTRY.](wizardentry.md) Pendant la configuration interactive, chaque événement utilisateur dans les pages de propriétés entraîne l’appel par l’Assistant Profil de la fonction de rappel du fournisseur basée sur le prototype [SERVICEWIZARDDLGPROC.](servicewizarddlgproc.md) 
  
Si un fournisseur de services ajouté au profil prend en charge les pages de l’Assistant Profil, il doit autoriser la configuration par programme du profil.
  

