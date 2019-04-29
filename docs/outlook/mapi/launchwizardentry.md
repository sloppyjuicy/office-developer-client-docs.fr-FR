---
title: LAUNCHWIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LAUNCHWIZARDENTRY
api_type:
- COM
ms.assetid: 5778dffa-f01b-46b3-9c19-862793740918
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c1509918eb587c17deebf95317cf57b4ab19928a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437384"
---
# <a name="launchwizardentry"></a>LAUNCHWIZARDENTRY

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction qui démarre l'application Assistant Profil pour l'ajout d'un ou plusieurs services de messagerie à un profil. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiwz. h  <br/> |
|Fonction définie implémentée par:  <br/> |MAPI  <br/> |
|Fonction définie appelée par:  <br/> |Applications clientes  <br/> |
   
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
  
> dans Handle de la fenêtre parente de l'appelant. Si l'appelant n'a pas de fenêtre parente, le paramètre _hParentWnd_ doit être null. 
    
 _ulFlags_
  
> dans Masque de réindicateur des indicateurs indiquant les options de l'Assistant Profil. Les indicateurs suivants peuvent être définis:
    
MAPI_PW_ADD_SERVICE_ONLY 
  
> L'Assistant Profil est d'ajouter uniquement les services de messagerie à l'aide du paramètre _lppszServiceNameToAdd_ et de ne pas afficher sa page de sélection des services de messagerie. 
    
MAPI_PW_FIRST_PROFILE 
  
> Le profil à créer est le premier de cette station de travail. 
    
MAPI_PW_HIDE_SERVICES_LIST 
  
> La page de l'Assistant Profil pour la sélection des services de message ne doit pas être affichée. 
    
MAPI_PW_LAUNCHED_BY_CONFIG 
  
> L'Assistant Profil a été lancé par l'application de configuration du panneau de configuration. 
    
MAPI_PW_PROVIDER_UI_ONLY 
  
> Seuls les boîtes de dialogue de configuration des fournisseurs de services doivent s'afficher et les pages de l'Assistant Profil ne doivent pas apparaître. Cet indicateur ne peut être défini que si l'indicateur MAPI_PW_ADD_SERVICE_ONLY est défini. 
    
 _lppszServiceNameToAdd_
  
> dans Pointeur vers un tableau de chaînes contenant les noms des services de message à ajouter au profil. Le tableau doit se terminer par une valeur NULL. 
    
 _cbBufferMax_
  
> dans Taille de la mémoire tampon vers laquelle pointe le paramètre _lpszNewProfileName_ . 
    
 _lpszNewProfileName_
  
> remarquer Pointeur vers une mémoire tampon de chaîne où la fonction basée sur **LAUNCHWIZARDENTRY** renvoie le nom du profil créé. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_CALL_FAILED 
  
> Une erreur d'origine inattendue ou inconnue a empêché l'opération de s'exécuter. Les possibilités incluent l'échec de l'initialisation du sous-système MAPI pour l'Assistant Profil, l'impossibilité d'accéder au profil par défaut et une erreur de retour dans la boîte de dialogue.
    
## <a name="remarks"></a>Remarques

L'implémentation MAPI du prototype de fonction **LAUNCHWIZARDENTRY** est le point d'entrée dans l'application Assistant Profil MAPI. MAPI nomme ce point d'entrée **LaunchWizard**. 
  
Lorsque l'indicateur MAPI_PW_ADD_SERVICE_ONLY est défini dans le paramètre _ulFlags_ , les règles suivantes s'appliquent: 
  
- L'indicateur MAPI_PW_LAUNCHED_BY_CONFIG empêche l'affichage de la page d'accueil. 
    
- Les indicateurs MAPI_PW_HIDE_SERVICES_LIST et MAPI_PW_PROVIDER_UI_ONLY ne sont utiles que s'il n'y a pas de profil par défaut. Dans ce cas, ces indicateurs déterminent la page de l'Assistant Profil qui doit être affichée. 
    
- Si un profil par défaut existe, aucune des pages de l'Assistant Profil n'est affichée. 
    
- S'il existe un profil par défaut, un seul service de messagerie est répertorié via le paramètre _lppszServiceNameToAdd_ , et ce service de messagerie se trouve déjà dans le profil par défaut, l'Assistant Profil renvoie S_OK sans rien ajouter au profil. 
    
Pour que chaque service de messagerie soit ajouté au profil, l'Assistant Profil appelle la fonction de point d'entrée du service en fonction du prototype [MSGSERVICEENTRY](msgserviceentry.md) . Pour chaque fournisseur de services sélectionné dans un service de messagerie à ajouter au profil, l'Assistant Profil appelle la fonction de point d'entrée du fournisseur en fonction du prototype [WIZARDENTRY](wizardentry.md) . Lors de la configuration interactive, chaque événement utilisateur dans les pages de propriétés fait en sorte que l'Assistant Profil appelle la fonction de rappel du fournisseur en fonction du prototype [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) . 
  
Si un fournisseur de services ajouté au profil prend en charge les pages de l'Assistant Profil, il doit autoriser la configuration par programme du profil.
  

