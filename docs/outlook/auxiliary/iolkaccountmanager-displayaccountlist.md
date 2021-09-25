---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Affiche la boîte de dialogue Paramètres compte ou Ajouter un nouveau compte.
ms.openlocfilehash: 22a9165fa5cd29e0f9da9de64c243806e6fb1712
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561921"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a>IOlkAccountManager::DisplayAccountList

Affiche la boîte de **dialogue Paramètres** compte ou Ajouter **un** nouveau compte. 
  
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

_hwnd_
  
> [in] Poignée de la fenêtre dans laquelle la boîte de dialogue affichée est modale. Peut être zéro.
    
_dwFlags_
  
> [in] Indicateurs pour modifier le comportement de l’affichage. 
    
   - **ACCTUI_NO_WARNING**: n’affichez pas l’avertissement signalant que les modifications ne prennent effet qu’une fois Outlook redémarrage. S’applique uniquement si l’application est en cours d’exécution in-process avec Outlook.exe.
    
   - **ACCTUI_SHOW_DATA_TAB**:afficher la boîte de **dialogue Paramètres** compte avec **l’onglet** Données sélectionné. Valide uniquement si **ACCTUI_SHOW_ACCTWIZARD** n’est pas définie. 
    
   - **ACCTUI_SHOW_ACCTWIZARD**: affiche la boîte de dialogue Ajouter **un nouveau** compte. 
    
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
|MAPI_E_CALL_FAILED  <br/> |La **boîte de dialogue Ajouter un nouveau compte** a renvoyé une erreur.  <br/> |
|MAPI_E_INVALID_PARAMETER  <br/> |Le  _paramètre cCategories_,  _rgclsidCategories_ ou  _pclsidType_ est non NULL.  <br/> |
|MAPI_E_USER_CANCEL  <br/> |La **boîte de dialogue Paramètres** compte a renvoyé une erreur.  <br/> |
   
## <a name="remarks"></a>Remarques

Les  _paramètres cCategories,_  _rgclsidCategories_ et  _pclsidType_ ne sont pas utilisés pour le moment et doivent être NULL.  _wszTitle n’est_ pas utilisé et doit également être NULL. 
  

