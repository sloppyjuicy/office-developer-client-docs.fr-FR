---
title: IMAPIFormContainer IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer
api_type:
- COM
ms.assetid: 437c8a75-1121-4919-8bd4-d57c0d6f4b9a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 208af28307a60615ecafda0992881c5df36aa56f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342188"
---
# <a name="imapiformcontainer--iunknown"></a>IMAPIFormContainer : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Gère les formulaires dans les bibliothèques de formulaires. Cette interface est utilisée pour créer des bibliothèques de formulaires propres à l'application. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm. h  <br/> |
|Exposé par:  <br/> |Objets conteneur de formulaire  <br/> |
|Implémenté par :  <br/> |Fournisseurs de bibliothèques de formulaires  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur de l'interface:  <br/> |IID_IMAPIFormContainer  <br/> |
|Type de pointeur:  <br/> |LPMAPIFORMCONTAINER  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[InstallForm](imapiformcontainer-installform.md) <br/> |Installe un formulaire dans un conteneur de formulaire.  <br/> |
|[RemoveForm](imapiformcontainer-removeform.md) <br/> |Supprime un formulaire particulier d'un conteneur de formulaires.  <br/> |
|[ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) <br/> |Résout une classe de message en son formulaire dans un conteneur de formulaire et renvoie un objet d'informations de formulaire pour ce formulaire.  <br/> |
|[ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |Résout un groupe de classes de message dans leurs formulaires dans un conteneur de formulaire et renvoie un tableau d'objets d'informations de formulaire pour ces formulaires.  <br/> |
|[CalcFormPropSet](imapiformcontainer-calcformpropset.md) <br/> |Renvoie un tableau des propriétés utilisées par tous les formulaires installés dans un conteneur de formulaire.  <br/> |
|[GetDisplay](imapiformcontainer-getdisplay.md) <br/> |Renvoie le nom d'affichage d'un conteneur de formulaire.  <br/> |
|[Généré](imapiformcontainer-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) contenant des informations sur l'erreur précédente qui s'est produite dans l'objet conteneur de formulaire.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

