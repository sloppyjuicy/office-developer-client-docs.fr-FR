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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d80671331c2760c574ab32d79115a352ee4bcf25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784534"
---
# <a name="launchwizardentry"></a>LAUNCHWIZARDENTRY

  
  
**S’applique à**: Outlook 
  
Définit une fonction qui démarre l’application Assistant profil en vue d’ajouter un ou plusieurs services de messagerie à un profil. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiwz.h  <br/> |
|Fonction implémentée par :  <br/> |MAPI  <br/> |
|Fonction appelée par :  <br/> |Applications clientes  <br/> |
   
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
  
> [in] Handle de fenêtre parent de l’appelant. Si l’appelant ne dispose pas d’une fenêtre parent, le paramètre _hParentWnd_ doit être NULL. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs indiquant les options de l’Assistant profil. Les indicateurs suivants peuvent être définis :
    
MAPI_PW_ADD_SERVICE_ONLY 
  
> L’Assistant profil consiste à ajouter uniquement les services de message répertoriés via le paramètre _lppszServiceNameToAdd_ et n’affiche pas la page de sélection de services de messagerie. 
    
MAPI_PW_FIRST_PROFILE 
  
> Le profil doit être créé est la première pour cette station de travail. 
    
MAPI_PW_HIDE_SERVICES_LIST 
  
> Page de l’Assistant profil de sélection de services de messagerie ne doit pas être affichée. 
    
MAPI_PW_LAUNCHED_BY_CONFIG 
  
> L’Assistant profil a été lancé par l’application de panneau de configuration. 
    
MAPI_PW_PROVIDER_UI_ONLY 
  
> Seules les boîtes de dialogue de configuration des fournisseurs de services doivent être affichés et pages de l’Assistant profil ne doivent pas apparaître. Cet indicateur peut être défini uniquement si l’indicateur MAPI_PW_ADD_SERVICE_ONLY est défini. 
    
 _lppszServiceNameToAdd_
  
> [in] Pointeur vers un tableau de chaînes contenant les noms des services de message à ajouter au profil. Le tableau doit se terminer par une valeur NULL. 
    
 _cbBufferMax_
  
> [in] Taille de la mémoire tampon vers laquelle pointe le paramètre _lpszNewProfileName_ . 
    
 _lpszNewProfileName_
  
> [out] Pointeur vers un tampon de chaîne dans laquelle la fonction **LAUNCHWIZARDENTRY** renvoie le nom du profil créé. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_CALL_FAILED 
  
> Une erreur d’origine inattendu ou inconnu a empêché l’opération de se terminer. Impossibilité d’accéder au profil par défaut et une erreur possibilités : échec d’initialisation du sous-système MAPI pour l’Assistant profil, renvoyer à partir de la boîte de dialogue.
    
## <a name="remarks"></a>Remarques

L’implémentation MAPI du prototype de la fonction **LAUNCHWIZARDENTRY** est le point d’entrée dans l’application Assistant profil MAPI. Ce point d’entrée **LaunchWizard**les noms MAPI. 
  
Lorsque l’indicateur MAPI_PW_ADD_SERVICE_ONLY est défini dans le paramètre _ulFlags_ , les règles suivantes s’appliquent : 
  
- L’indicateur MAPI_PW_LAUNCHED_BY_CONFIG empêche la page d’accueil de s’afficher. 
    
- Les indicateurs MAPI_PW_HIDE_SERVICES_LIST et MAPI_PW_PROVIDER_UI_ONLY sont utiles uniquement lorsqu’il n’existe aucun profil par défaut. Dans ce cas, ces indicateurs déterminent quel Assistant profil page doit s’afficher. 
    
- Si un profil par défaut existe, aucune des pages de l’Assistant profil doivent être affichées. 
    
- Si un profil par défaut existe, service qu’un message est répertorié par le biais du paramètre _lppszServiceNameToAdd_ , et que le service de message est déjà dans le profil par défaut, l’Assistant profil renvoie S_OK sans rien ajouter au profil. 
    
Pour chaque service de message à ajouter au profil, l’Assistant profil appelle la fonction de point d’entrée du service basée sur le prototype [MSGSERVICEENTRY](msgserviceentry.md) . Pour chaque fournisseur de services sélectionné à partir d’un service de message à ajouter au profil, l’Assistant profil appelle la fonction de point d’entrée du fournisseur basée sur le prototype [WIZARDENTRY](wizardentry.md) . Lors de la configuration interactive, tous les événements dans les pages de propriétés utilisateur, l’Assistant de profil appeler la fonction de rappel du fournisseur basée sur le prototype [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) . 
  
Si un fournisseur de services en cours d’ajout au profil prend en charge les pages de l’Assistant profil, il doit autoriser la configuration par programme du profil.
  

