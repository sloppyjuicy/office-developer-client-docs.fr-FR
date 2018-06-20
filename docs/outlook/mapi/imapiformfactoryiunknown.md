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
ms.openlocfilehash: 651ef6a7c1af70c75a85e13414c4fd7632d30290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783792"
---
# <a name="imapiformfactory--iunknown"></a>IMAPIFormFactory : IUnknown

  
  
**S’applique à**: Outlook 
  
Prend en charge l’utilisation des formulaires d’exécution configurables dans des environnements informatiques distribués. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm.h  <br/> |
|Exposés par :  <br/> |Objets de fabrique de formulaire  <br/> |
|Implémentée par :  <br/> |Serveurs de formulaire  <br/> |
|Appelée par :  <br/> |Visionneuses de formulaire  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIFormFactory  <br/> |
|Type de pointeur :  <br/> |LPMAPIFORMFACTORY  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[CreateClassFactory](imapiformfactory-createclassfactory.md) <br/> |Renvoie un objet de fabrique de classe pour le formulaire.  <br/> |
|[GetLastError](imapiformfactory-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente à l’objet de fabrique de formulaire.  <br/> |
|[LockServer](imapiformfactory-lockserver.md) <br/> |Tenir à jour un serveur de formulaire ouvert en mémoire.  <br/> |
   
## <a name="remarks"></a>Remarques

L’interface **IMAPIFormFactory** repose sur l’interface [IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) et les objets qui implémentent **IMAPIFormFactory** doivent également hériter de **IClassFactory**.
  
 **IMAPIFormFactory** est l’interface visionneuses de formulaire permet de créer de nouveaux objets de formulaire lorsqu’un serveur de formulaire prend en charge plus d’une classe de message (autrement dit, plus d’un type d’objet de formulaire). 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

