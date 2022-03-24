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
ms.openlocfilehash: 158e44e482035e97a899945a6862eadbc66336eb
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63725287"
---
# <a name="imapiformfactory--iunknown"></a>IMAPIFormFactory : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prend en charge l’utilisation de formulaires d’utilisation configurables dans les environnements informatiques distribués. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Objets fabrique de formulaires  <br/> |
|Implémenté par :  <br/> |Serveurs de formulaires  <br/> |
|Appelé par :  <br/> |Visionneuses de formulaires  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIFormFactory  <br/> |
|Type de pointeur :  <br/> |LPMAPIFORMFACTORY  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Propriété |Valeur |
|:-----|:-----|
|[CreateClassFactory](imapiformfactory-createclassfactory.md) <br/> |Renvoie un objet fabrique de classes pour le formulaire. |
|[GetLastError](imapiformfactory-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite sur l’objet de fabrique de formulaire. |
|[LockServer](imapiformfactory-lockserver.md) <br/> |Conserve un serveur de formulaire ouvert en mémoire. |
   
## <a name="remarks"></a>Remarques

**L’interface IMAPIFormFactory** est basée sur l’interface [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) et les objets qui implémentent **IMAPIFormFactory** doivent également hériter **d’IClassFactory**.
  
 **IMAPIFormFactory** est l’interface que les visionneuses de formulaires utilisent pour créer des objets de formulaire lorsqu’un serveur de formulaires prend en charge plusieurs classes de message (c’est-à-dire, plusieurs types d’objet de formulaire). 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

