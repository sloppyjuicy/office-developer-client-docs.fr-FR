---
title: IMAPIFormFactory IUnknown
description: IMAPIFormFactoryIUnknown prend en charge l’utilisation de formulaires d’exécution configurables dans des environnements informatiques distribués.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormFactory
api_type:
- COM
ms.assetid: 637be364-c393-430a-84b3-2c96aa553c22
ms.openlocfilehash: b1cda9fd219677934a7cd31bfbfbdb88a8f3e895
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812193"
---
# <a name="imapiformfactory--iunknown"></a>IMAPIFormFactory : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prend en charge l’utilisation de formulaires d’exécution configurables dans des environnements informatiques distribués. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Objets de fabrique de formulaires  <br/> |
|Implémenté par :  <br/> |Serveurs de formulaires  <br/> |
|Appelé par :  <br/> |Visionneuses de formulaires  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIFormFactory  <br/> |
|Type de pointeur :  <br/> |LPMAPIFORMFACTORY  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Propriété |Valeur |
|:-----|:-----|
|[CreateClassFactory](imapiformfactory-createclassfactory.md) <br/> |Retourne un objet de fabrique de classes pour le formulaire. |
|[Getlasterror](imapiformfactory-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite dans l’objet de fabrique de formulaires. |
|[LockServer](imapiformfactory-lockserver.md) <br/> |Conserve un serveur de formulaire ouvert en mémoire. |
   
## <a name="remarks"></a>Remarques

**L’interface IMAPIFormFactory** est basée sur l’interface [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) et les objets qui implémentent **IMAPIFormFactory** doivent également hériter d’IClassFactory.
  
 **IMAPIFormFactory** est l’interface utilisée par les visionneuses de formulaires pour créer des objets de formulaire lorsqu’un serveur de formulaires prend en charge plusieurs classes de message (autrement dit, plusieurs types d’objet de formulaire). 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

