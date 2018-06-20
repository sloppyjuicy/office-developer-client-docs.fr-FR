---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Affiche la boîte de dialogue Ajouter un nouveau compte ou paramètres de compte.
ms.openlocfilehash: 3c7c433eb4d8f316d32b6cd12bbbbb0e1a1cee43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782721"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a>IOlkAccountManager::DisplayAccountList

Affiche la boîte de dialogue les **Paramètres de compte** ou **Ajouter un nouveau compte** . 
  
## <a name="quick-info"></a>Informations rapides

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::DisplayAccountList ( 
    HWND hwnd,
    DWORD dwFlags,
    LPCWSTR wszTitle,
    DWORD cCategories,
    const CLSID * rgclsidCategories,
    const CLSID * pclsidType
);

```

## <a name="parameters"></a>Paramètres

_HWND_
  
> [in] Handle vers la fenêtre à laquelle la boîte de dialogue qui s’affiche est modale. Peut être égal à zéro.
    
_dwFlags_
  
> [in] Indicateurs pour modifier le comportement de l’affichage. 
    
   - **ACCTUI_NO_WARNING**: ne pas afficher l’avertissement que les modifications ne prendront effet qu’après le redémarrage d’Outlook. S’applique uniquement si l’application est en cours d’exécution en cours avec Outlook.exe.
    
   - **ACCTUI_SHOW_DATA_TAB**— affiche la boîte de dialogue **Paramètres du compte** avec l’onglet **données** est sélectionné. Valide uniquement si **ACCTUI_SHOW_ACCTWIZARD** n’est pas définie. 
    
   - **ACCTUI_SHOW_ACCTWIZARD**— affiche la boîte de dialogue **Ajouter un nouveau compte** . 
    
_wszTitle_
  
> [in] Ce paramètre n’est pas utilisé et doit être NULL.
    
_cCategories_
  
> [in] Ce paramètre n’est pas utilisé et doit être NULL. 
    
_rgclsidCategories_
  
> [in] Ce paramètre n’est pas utilisé et doit être NULL.
    
_pclsidType_
  
> [in] Ce paramètre n’est pas utilisé et doit être NULL.
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L’appel a réussi.  <br/> |
|E_ACCT_UI_BUSY  <br/> |La boîte de dialogue n’a pas pu être créée.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |La boîte de dialogue **Ajouter un nouveau compte** a renvoyé une erreur.  <br/> |
|MAPI_E_INVALID_PARAMETER  <br/> |Le paramètre _cCategories_, _rgclsidCategories_ou _pclsidType_ est non nulle.  <br/> |
|MAPI_E_USER_CANCEL  <br/> |La boîte de dialogue **Paramètres du compte** a renvoyé une erreur.  <br/> |
   
## <a name="remarks"></a>Remarques

Les paramètres _cCategories_, _rgclsidCategories_et _pclsidType_ ne sont pas utilisés pour l’instant et doivent être NULL.  _wszTitle_ n’est pas utilisé et doit également être NULL. 
  

