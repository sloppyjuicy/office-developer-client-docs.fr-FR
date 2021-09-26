---
title: IMAPIFormFactory IUnknown
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d9ab1c92faa2780680d198939712163a79e3b3ea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610600"
---
# <a name="imapiformfactory--iunknown"></a>IMAPIFormFactory : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prend en charge l’utilisation de formulaires d’utilisation configurables dans les environnements informatiques distribués. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Objets fabrique de formulaires  <br/> |
|Implémenté par :  <br/> |Serveurs de formulaires  <br/> |
|Appelé par :  <br/> |Visionneuses de formulaires  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIFormFactory  <br/> |
|Type de pointeur :  <br/> |LPMAPIFORMFACTORY  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[CreateClassFactory](imapiformfactory-createclassfactory.md) <br/> |Renvoie un objet fabrique de classes pour le formulaire.  <br/> |
|[GetLastError](imapiformfactory-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite sur l’objet de fabrique de formulaire.  <br/> |
|[LockServer](imapiformfactory-lockserver.md) <br/> |Conserve un serveur de formulaire ouvert en mémoire.  <br/> |
   
## <a name="remarks"></a>Remarques

**L’interface IMAPIFormFactory** est basée sur l’interface [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) et les objets qui implémentent **IMAPIFormFactory** doivent également hériter de **IClassFactory**.
  
 **IMAPIFormFactory** est l’interface que les visionneuses de formulaires utilisent pour créer des objets de formulaire lorsqu’un serveur de formulaires prend en charge plusieurs classes de message (c’est-à-dire, plusieurs types d’objet de formulaire). 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

