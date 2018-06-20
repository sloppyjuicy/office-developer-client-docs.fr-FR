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
ms.openlocfilehash: ef9b99f06b62fd361bb780debb527ec2d7457589
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783837"
---
# <a name="imapiformmgrselectformcontainer"></a>IMAPIFormMgr::SelectFormContainer

  
  
**S’applique à**: Outlook 
  
Présente une boîte de dialogue qui permet à l’utilisateur sélectionner un conteneur de formulaire et renvoie une interface pour l’objet conteneur de l’utilisateur sélectionné.
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Handle vers la fenêtre parente de la boîte de dialogue qui s’affiche. 
    
 _ulFlags_
  
> [in] Un masque de bits d’indicateurs qui contrôle la façon dont la bibliothèque de formulaires est activée (autrement dit, comment le conteneur de formulaire est sélectionné). Les indicateurs suivants peuvent être définis :
    
MAPIFORM_SELECT_ALL_REGISTRIES 
  
> Effectuer une sélection à partir de tous les conteneurs. Il s’agit du type de sélection par défaut. 
    
MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY 
  
> Sélection peut être effectuée qu’à partir de conteneurs de dossiers.
    
MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY 
  
> Sélection peut être effectuée qu’à partir de conteneurs qui ne sont pas associés à des dossiers.
    
 _lppfcnt_
  
> [out] Pointeur vers un pointeur vers l’interface retournée. Cette interface n’est pour l’objet conteneur qui est sélectionné par l’utilisateur.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

En général, les visionneuses de formulaire appelez la méthode **IMAPIFormMgr::SelectFormContainer** pour sélectionner un conteneur de formulaire dans lequel un formulaire est installé. **SelectFormContainer** ne peut pas être utilisée pour sélectionner le conteneur de formulaire local, qui a la valeur HFRMREG_LOCAL. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSelectFormContainer  <br/> |MFCMAPI utilise la méthode **IMAPIFormMgr::SelectFormContainer** pour sélectionner un conteneur de formulaire avant l’affichage de son contenu.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

