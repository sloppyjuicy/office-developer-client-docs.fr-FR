---
title: IMAPIFormFactory IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory
api_type:
- COM
ms.assetid: 637be364-c393-430a-84b3-2c96aa553c22
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c60b542852653bd617b5b9f604bbc44d575e5cb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342118"
---
# <a name="imapiformfactory--iunknown"></a>IMAPIFormFactory : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prend en charge l'utilisation de formulaires d'exécution configurables dans les environnements informatiques distribués. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm. h  <br/> |
|Exposé par:  <br/> |Objets de fabrique de formulaires  <br/> |
|Implémenté par :  <br/> |Serveurs de formulaires  <br/> |
|Appelé par :  <br/> |Visionneuses de formulaires  <br/> |
|Identificateur de l'interface:  <br/> |IID_IMAPIFormFactory  <br/> |
|Type de pointeur:  <br/> |LPMAPIFORMFACTORY  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[CreateClassFactory](imapiformfactory-createclassfactory.md) <br/> |Renvoie un objet de fabrique de classe pour le formulaire.  <br/> |
|[Généré](imapiformfactory-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur précédente qui s'est produite dans l'objet Factory de formulaire.  <br/> |
|[LockServer](imapiformfactory-lockserver.md) <br/> |Conserve un serveur de formulaires ouvert en mémoire.  <br/> |
   
## <a name="remarks"></a>Remarques

L'interface **IMAPIFormFactory** est basée sur l'interface [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) , et les objets qui implémentent **IMAPIFormFactory** doivent également hériter de **IClassFactory**.
  
 **IMAPIFormFactory** est l'interface utilisée par les visionneuses de formulaires pour créer des objets de formulaire lorsqu'un serveur de formulaire prend en charge plusieurs classes de message (autrement dit, plusieurs types d'objet de formulaire). 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

