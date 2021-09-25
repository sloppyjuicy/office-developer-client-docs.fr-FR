---
title: IMAPIFormContainer IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormContainer
api_type:
- COM
ms.assetid: 437c8a75-1121-4919-8bd4-d57c0d6f4b9a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7691cdaf21ae98b963aa63e0af7ab2c151a4f3da
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576022"
---
# <a name="imapiformcontainer--iunknown"></a>IMAPIFormContainer : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Gère les formulaires dans les bibliothèques de formulaires. Cette interface permet de créer des bibliothèques de formulaires spécifiques à l’application. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Objets conteneur de formulaires  <br/> |
|Implémenté par :  <br/> |Fournisseurs de bibliothèques de formulaires  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIFormContainer  <br/> |
|Type de pointeur :  <br/> |LPMAPIFORMCONTAINER  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[InstallForm](imapiformcontainer-installform.md) <br/> |Installe un formulaire dans un conteneur de formulaires.  <br/> |
|[RemoveForm](imapiformcontainer-removeform.md) <br/> |Supprime un formulaire particulier d’un conteneur de formulaires.  <br/> |
|[ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) <br/> |Résout une classe de message dans son formulaire dans un conteneur de formulaires et renvoie un objet d’informations de formulaire pour ce formulaire.  <br/> |
|[ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |Résout un groupe de classes de message dans leurs formulaires dans un conteneur de formulaires et renvoie un tableau d’objets d’informations de formulaire pour ces formulaires.  <br/> |
|[CalcFormPropSet](imapiformcontainer-calcformpropset.md) <br/> |Renvoie un tableau des propriétés utilisées par tous les formulaires installés dans un conteneur de formulaires.  <br/> |
|[GetDisplay](imapiformcontainer-getdisplay.md) <br/> |Renvoie le nom complet d’un conteneur de formulaire.  <br/> |
|[GetLastError](imapiformcontainer-getlasterror.md) <br/> |Renvoie une [structure MAPIERROR contenant](mapierror.md) des informations sur l’erreur précédente qui s’est produite sur l’objet conteneur de formulaire.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

