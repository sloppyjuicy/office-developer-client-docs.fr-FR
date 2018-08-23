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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b4eaf424bd22f5cb7f40778d81a18cca0ef1dcc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581516"
---
# <a name="imapiformmgr--iunknown"></a>IMAPIFormMgr : IUnknown

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Permet les visionneuses de formulaire obtenir des informations sur et activer des serveurs de formulaire. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm.h  <br/> |
|Exposés par :  <br/> |Objets Gestionnaire de formulaire  <br/> |
|Implémentée par :  <br/> |Fournisseurs de bibliothèques de formulaires  <br/> |
|Appelée par :  <br/> |Visionneuses de formulaire  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIFormMgr  <br/> |
|Type de pointeur :  <br/> |LPMAPIFORMMGR  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[LoadForm](imapiformmgr-loadform.md) <br/> |Démarre un formulaire pour ouvrir un message existant.  <br/> |
|[ResolveMessageClass](imapiformmgr-resolvemessageclass.md) <br/> |Associe une classe de message à sa forme au sein d’un conteneur de formulaire et renvoie un objet d’informations de formulaire pour ce formulaire.  <br/> |
|[ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |Résout un groupe de classes de message à leurs formulaires dans un conteneur de formulaire et renvoie un tableau de formulaire objets des informations pour les formulaires.  <br/> |
|[CalcFormPropSet](imapiformmgr-calcformpropset.md) <br/> |Renvoie un tableau des propriétés qui utilise un groupe de formulaires.  <br/> |
|[CreateForm](imapiformmgr-createform.md) <br/> |Ouvre un formulaire pour créer un nouveau message en fonction de la classe de message du formulaire.  <br/> |
|[SelectForm](imapiformmgr-selectform.md) <br/> |Affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner un formulaire et renvoie un objet d’informations de formulaire qui décrit ce formulaire.  <br/> |
|[SelectMultipleForms](imapiformmgr-selectmultipleforms.md) <br/> |Affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner plusieurs formulaires et renvoie un tableau de formulaire objets informations décrivant les formulaires.  <br/> |
|[SelectFormContainer](imapiformmgr-selectformcontainer.md) <br/> |Présente une boîte de dialogue qui permet à l’utilisateur sélectionner un conteneur de formulaire et renvoie une interface pour l’objet conteneur de l’utilisateur sélectionné.  <br/> |
|[OpenFormContainer](imapiformmgr-openformcontainer.md) <br/> |Ouvre une interface [IMAPIFormContainer](imapiformcontaineriunknown.md) pour un conteneur de formulaire spécifique.  <br/> |
|[PrepareForm](imapiformmgr-prepareform.md) <br/> |Télécharge un formulaire d’ouverture.  <br/> |
|[IsInConflict](imapiformmgr-isinconflict.md) <br/> |Détermine si un formulaire peut gérer son propre conflits de message.  <br/> |
|[GetLastError](imapiformmgr-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente à l’objet de gestionnaire de formulaire.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

