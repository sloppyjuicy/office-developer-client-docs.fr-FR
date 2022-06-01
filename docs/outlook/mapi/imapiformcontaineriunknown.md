---
title: IMAPIFormContainer IUnknown
description: IMAPIFormContainerIUnknown gère les formulaires dans les bibliothèques de formulaires. Cette interface est utilisée pour créer des bibliothèques de formulaires spécifiques à l’application.
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
ms.openlocfilehash: add54dc76477fedca0455005ddd8c1a505796564
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816156"
---
# <a name="imapiformcontainer--iunknown"></a>IMAPIFormContainer : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Gère les formulaires dans les bibliothèques de formulaires. Cette interface est utilisée pour créer des bibliothèques de formulaires spécifiques à l’application. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Objets conteneur de formulaire  <br/> |
|Implémenté par :  <br/> |Fournisseurs de bibliothèques de formulaires  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIFormContainer  <br/> |
|Type de pointeur :  <br/> |LPMAPIFORMCONTAINER  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member |Description |
|:-----|:-----|
|[InstallForm](imapiformcontainer-installform.md) <br/> |Installe un formulaire dans un conteneur de formulaires. |
|[RemoveForm](imapiformcontainer-removeform.md) <br/> |Supprime un formulaire particulier d’un conteneur de formulaires. |
|[ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) <br/> |Résout une classe de message dans son formulaire dans un conteneur de formulaires et retourne un objet d’informations de formulaire pour ce formulaire. |
|[ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |Résout un groupe de classes de messages en leurs formulaires dans un conteneur de formulaires et retourne un tableau d’objets d’informations de formulaire pour ces formulaires. |
|[CalcFormPropSet](imapiformcontainer-calcformpropset.md) <br/> |Retourne un tableau des propriétés utilisées par tous les formulaires installés dans un conteneur de formulaires. |
|[GetDisplay](imapiformcontainer-getdisplay.md) <br/> |Retourne le nom complet d’un conteneur de formulaires. |
|[Getlasterror](imapiformcontainer-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) contenant des informations sur l’erreur précédente qui s’est produite dans l’objet conteneur de formulaire. |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

