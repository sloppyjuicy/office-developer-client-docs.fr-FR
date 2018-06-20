---
title: IMAPIFormContainerResolveMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMessageClass
api_type:
- COM
ms.assetid: 9ce13f11-5787-4ea5-a84f-b1e3824529ee
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 713a177d5ceddf5fd4d97a0e35d87b2250748faf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783775"
---
# <a name="imapiformcontainerresolvemessageclass"></a>IMAPIFormContainer::ResolveMessageClass

  
  
**S’applique à**: Outlook 
  
Résout une classe de message à sa forme dans un conteneur de formulaire et renvoie un objet d’informations de formulaire pour ce formulaire.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a>Paramètres

 _szMessageClass_
  
> [in] Chaîne qui nomme la classe de message en cours de résolution. Noms de classe de message sont toujours des chaînes ANSI, Unicode jamais.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont la classe de message est résolue. Vous pouvez définir l’indicateur suivant :
    
MAPIFORM_EXACTMATCH 
  
> Seules les chaînes de classe de message qui sont une correspondance exacte doivent être résolus.
    
 _ppforminfo_
  
> [out] Pointeur vers un pointeur vers l’objet d’informations de formulaire renvoyé.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NOT_FOUND 
  
> La classe de message transmise dans le paramètre _szMessageClass_ ne correspond pas à la classe de message pour n’importe quel formulaire dans le conteneur du formulaire. 
    
## <a name="remarks"></a>Remarques

Applications clientes appellent la méthode **IMAPIFormContainer::ResolveMessageClass** pour résoudre une classe de message à un formulaire dans un conteneur de formulaire. L’écran informations objet renvoyé dans le paramètre _ppforminfo_ fournit plus accès aux propriétés du formulaire avec la classe de message donné. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Pour résoudre une classe de message à un formulaire, passez le nom de la classe de message pour être résolu (par exemple, `IPM.HelpDesk.Software`). Pour forcer la résolution à être exact (autrement dit, pour empêcher la résolution à une classe de base de la classe de message), l’indicateur MAPIFORM_EXACTMATCH peut être passé dans le paramètre _ulFlags_ . 
  
L’identificateur de classe pour la classe de message résolu est renvoyée dans le cadre de l’objet d’informations de formulaire. Ne pensez pas que l’identificateur de classe existe dans la bibliothèque OLE jusqu'à après l’appel de méthode le [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) ou [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMessageClass  <br/> |MFCMAPI utilise la méthode **IMAPIFormContainer::ResolveMessageClass** pour localiser un formulaire qui est associé à une classe de message.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

