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
ms.openlocfilehash: 39f255a277403073132dfd3cd21c995eefe904c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783777"
---
# <a name="imapiformcontainer--iunknown"></a>IMAPIFormContainer : IUnknown

  
  
**S’applique à**: Outlook 
  
Gère les formulaires dans les bibliothèques de formulaires. Cette interface est utilisée pour créer des bibliothèques de formulaires spécifique à l’application. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm.h  <br/> |
|Exposés par :  <br/> |Objets conteneurs de formulaire  <br/> |
|Implémentée par :  <br/> |Fournisseurs de bibliothèques de formulaires  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIFormContainer  <br/> |
|Type de pointeur :  <br/> |LPMAPIFORMCONTAINER  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[InstallForm](imapiformcontainer-installform.md) <br/> |Installe un formulaire dans un conteneur de formulaire.  <br/> |
|[RemoveForm](imapiformcontainer-removeform.md) <br/> |Supprime un formulaire particulier à partir d’un conteneur de formulaire.  <br/> |
|[ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) <br/> |Résout une classe de message à sa forme dans un conteneur de formulaire et renvoie un objet d’informations de formulaire pour ce formulaire.  <br/> |
|[ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |Résout un groupe de classes de message à leurs formulaires dans un conteneur de formulaire et renvoie un tableau de formulaire objets des informations pour les formulaires.  <br/> |
|[CalcFormPropSet](imapiformcontainer-calcformpropset.md) <br/> |Renvoie un tableau de propriétés utilisées par tous les formulaires installés dans un conteneur de formulaire.  <br/> |
|[GetDisplay](imapiformcontainer-getdisplay.md) <br/> |Renvoie le nom complet d’un conteneur de formulaire.  <br/> |
|[GetLastError](imapiformcontainer-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) contenant des informations sur l’erreur précédente à l’objet conteneur de formulaire en cours.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

