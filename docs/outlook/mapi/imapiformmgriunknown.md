---
title: IMAPIFormMgr IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr
api_type:
- COM
ms.assetid: 8cbd1a42-7de6-43e0-8c77-7711773843d5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fbe6dc9364ee953661d574b70bcd225abcfe7a81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413058"
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

