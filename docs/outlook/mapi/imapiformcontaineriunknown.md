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
ms.openlocfilehash: 1114a3e7c4c38184a43c89ae9f734be1062ed1ff
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63724341"
---
# <a name="imapiformcontainer--iunknown"></a>IMAPIFormContainer : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Gère les formulaires dans les bibliothèques de formulaires. Cette interface permet de créer des bibliothèques de formulaires spécifiques à l’application. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Objets conteneur de formulaires  <br/> |
|Implémenté par :  <br/> |Fournisseurs de bibliothèques de formulaires  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIFormContainer  <br/> |
|Type de pointeur :  <br/> |LPMAPIFORMCONTAINER  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member |Description |
|:-----|:-----|
|[InstallForm](imapiformcontainer-installform.md) <br/> |Installe un formulaire dans un conteneur de formulaires. |
|[RemoveForm](imapiformcontainer-removeform.md) <br/> |Supprime un formulaire particulier d’un conteneur de formulaires. |
|[ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) <br/> |Résout une classe de message dans son formulaire dans un conteneur de formulaires et renvoie un objet d’informations de formulaire pour ce formulaire. |
|[ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |Résout un groupe de classes de message dans leurs formulaires dans un conteneur de formulaires et renvoie un tableau d’objets d’informations de formulaire pour ces formulaires. |
|[CalcFormPropSet](imapiformcontainer-calcformpropset.md) <br/> |Renvoie un tableau des propriétés utilisées par tous les formulaires installés dans un conteneur de formulaires. |
|[GetDisplay](imapiformcontainer-getdisplay.md) <br/> |Renvoie le nom complet d’un conteneur de formulaires. |
|[GetLastError](imapiformcontainer-getlasterror.md) <br/> |Renvoie une [structure MAPIERROR contenant](mapierror.md) des informations sur l’erreur précédente qui s’est produite sur l’objet conteneur de formulaire. |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

