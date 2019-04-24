---
title: IMAPIFormMgrSelectFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: c33daad6-52c4-4968-ac56-415178c9bf12
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bfddc24e6a9c7cf8bdeae1e5ea730ecdb116f564
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321587"
---
# <a name="imapiformmgrselectformcontainer"></a>IMAPIFormMgr::SelectFormContainer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Affiche une boîte de dialogue qui permet à l'utilisateur de sélectionner un conteneur de formulaires et renvoie une interface pour l'objet conteneur sélectionné par l'utilisateur.
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> dans Handle de la fenêtre parent de la boîte de dialogue affichée. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont la bibliothèque de formulaires est sélectionnée (autrement dit, mode de sélection du conteneur de formulaire). Les indicateurs suivants peuvent être définis:
    
MAPIFORM_SELECT_ALL_REGISTRIES 
  
> La sélection peut être effectuée à partir de tous les conteneurs. Il s'agit du type de sélection par défaut. 
    
MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY 
  
> La sélection peut uniquement être effectuée à partir de conteneurs de dossiers.
    
MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY 
  
> La sélection peut uniquement être effectuée à partir de conteneurs qui ne sont pas associés à des dossiers.
    
 _lppfcnt_
  
> remarquer Pointeur vers un pointeur vers l'interface renvoyée. Cette interface est destinée à l'objet conteneur sélectionné par l'utilisateur.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent généralement la méthode **IMAPIFormMgr:: SelectFormContainer** pour sélectionner un conteneur de formulaires dans lequel un formulaire est installé. **SelectFormContainer** ne peut pas être utilisé pour sélectionner le conteneur de formulaire local, qui a la valeur HFRMREG_LOCAL. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnSelectFormContainer  <br/> |MFCMAPI utilise la méthode **IMAPIFormMgr:: SelectFormContainer** pour sélectionner un conteneur de formulaire avant de restituer son contenu.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

