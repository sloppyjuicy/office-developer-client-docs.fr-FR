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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bfddc24e6a9c7cf8bdeae1e5ea730ecdb116f564
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428591"
---
# <a name="imapiformmgrselectformcontainer"></a>IMAPIFormMgr::SelectFormContainer

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Présente une boîte de dialogue qui permet à l’utilisateur de sélectionner un conteneur de formulaire et renvoie une interface pour l’objet conteneur sélectionné par l’utilisateur.
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Poignée vers la fenêtre parente de la boîte de dialogue affichée. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont la bibliothèque de formulaires est sélectionnée (autrement dit, la façon dont le conteneur de formulaire est sélectionné). Les indicateurs suivants peuvent être définies :
    
MAPIFORM_SELECT_ALL_REGISTRIES 
  
> La sélection peut être réalisée à partir de tous les conteneurs. Il s’agit du type de sélection par défaut. 
    
MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY 
  
> La sélection ne peut être réalisée qu’à partir de conteneurs de dossiers.
    
MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY 
  
> La sélection peut être réalisée uniquement à partir de conteneurs qui ne sont pas associés à des dossiers.
    
 _lppfcnt_
  
> [out] Pointeur vers un pointeur vers l’interface renvoyée. Cette interface est pour l’objet conteneur sélectionné par l’utilisateur.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaire appellent généralement la méthode **IMAPIFormMgr::SelectFormContainer** pour sélectionner un conteneur de formulaire dans lequel un formulaire est installé. **SelectFormContainer ne peut** pas être utilisé pour sélectionner le conteneur de formulaire local, dont la valeur est HFRMREG_LOCAL. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSelectFormContainer  <br/> |MFCMAPI utilise la méthode **IMAPIFormMgr::SelectFormContainer** pour sélectionner un conteneur de formulaire avant d’en rendre le contenu.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

