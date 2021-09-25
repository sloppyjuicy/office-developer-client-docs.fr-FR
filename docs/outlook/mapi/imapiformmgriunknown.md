---
title: IMAPIFormMgr IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgr
api_type:
- COM
ms.assetid: 8cbd1a42-7de6-43e0-8c77-7711773843d5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e2d493dd4a0a244363a5405701498c5a96c76870
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571772"
---
# <a name="imapiformmgr--iunknown"></a>IMAPIFormMgr : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet aux visionneuses de formulaires d’obtenir des informations sur les serveurs de formulaires et d’en activer. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Objets du gestionnaire de formulaires  <br/> |
|Implémenté par :  <br/> |Fournisseurs de bibliothèques de formulaires  <br/> |
|Appelé par :  <br/> |Visionneuses de formulaires  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIFormMgr  <br/> |
|Type de pointeur :  <br/> |LPMAPIFORMMGR  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[LoadForm](imapiformmgr-loadform.md) <br/> |Démarre un formulaire pour ouvrir un message existant.  <br/> |
|[ResolveMessageClass](imapiformmgr-resolvemessageclass.md) <br/> |Résout une classe de message dans son formulaire dans un conteneur de formulaire et renvoie un objet d’informations de formulaire pour ce formulaire.  <br/> |
|[ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |Résout un groupe de classes de message dans leurs formulaires dans un conteneur de formulaires et renvoie un tableau d’objets d’informations de formulaire pour ces formulaires.  <br/> |
|[CalcFormPropSet](imapiformmgr-calcformpropset.md) <br/> |Renvoie un tableau des propriétés qu’un groupe de formulaires utilise.  <br/> |
|[CreateForm](imapiformmgr-createform.md) <br/> |Lance un formulaire pour créer un message basé sur la classe de message du formulaire.  <br/> |
|[SelectForm](imapiformmgr-selectform.md) <br/> |Présente une boîte de dialogue qui permet à l’utilisateur de sélectionner un formulaire et renvoie un objet d’informations sur le formulaire qui décrit ce formulaire.  <br/> |
|[SelectMultipleForms](imapiformmgr-selectmultipleforms.md) <br/> |Présente une boîte de dialogue qui permet à l’utilisateur de sélectionner plusieurs formulaires et renvoie un tableau d’objets d’informations sur les formulaires qui décrivent ces formulaires.  <br/> |
|[SelectFormContainer](imapiformmgr-selectformcontainer.md) <br/> |Présente une boîte de dialogue qui permet à l’utilisateur de sélectionner un conteneur de formulaire et renvoie une interface pour l’objet conteneur sélectionné par l’utilisateur.  <br/> |
|[OpenFormContainer](imapiformmgr-openformcontainer.md) <br/> |Ouvre une interface [IMAPIFormContainer](imapiformcontaineriunknown.md) pour un conteneur de formulaire spécifique.  <br/> |
|[PrepareForm](imapiformmgr-prepareform.md) <br/> |Télécharge un formulaire à ouvrir.  <br/> |
|[IsInConflict](imapiformmgr-isinconflict.md) <br/> |Détermine si un formulaire peut gérer ses propres conflits de messages.  <br/> |
|[GetLastError](imapiformmgr-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite sur l’objet gestionnaire de formulaires.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

