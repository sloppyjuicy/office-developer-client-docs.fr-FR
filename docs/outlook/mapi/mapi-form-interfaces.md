---
title: Interfaces de formulaires MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f37d398167e8210a2fd67ff08e63572eb6c9db9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585723"
---
# <a name="mapi-form-interfaces"></a>Interfaces de formulaires MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
MAPI définit les interfaces suivantes relatives aux formulaires.
  
|**Nom de l’interface**|**Description**|
|:-----|:-----|
|[IMAPIForm](imapiformiunknown.md) <br/> |Manipule les objets de formulaire et gère les commandes objet.  <br/> |
|[IMAPIFormAdviseSink](imapiformadvisesinkiunknown.md) <br/> |Détermine si l’objet form peut gérer le message suivant et modifie l’état suivant ou précédent de l’objet form.  <br/> |
|[IMAPIFormContainer](imapiformcontaineriunknown.md) <br/> |Prend en charge d’installation, désinstallation et la résolution des serveurs de formulaire par rapport à un conteneur de formulaire spécifique.  <br/> |
|[IMAPIFormFactory](imapiformfactoryiunknown.md) <br/> |Prend en charge l’utilisation de serveurs configurable exécution du formulaire.  <br/> |
|[IMAPIFormInfo](imapiforminfoimapiprop.md) <br/> |Permet aux applications de client travailler avec les propriétés qui sont spécifiques à une classe de message.  <br/> |
|[IMAPIFormMgr](imapiformmgriunknown.md) <br/> |Permet aux applications clientes obtenir des informations sur les serveurs de formulaire active des serveurs de formulaire et installe les serveurs de formulaire dans le système de messagerie.  <br/> |
|[IMAPIMessageSite](imapimessagesiteiunknown.md) <br/> |Utilisé pour manipuler les messages associés aux objets de formulaire.  <br/> |
|[IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) <br/> |Avertit les applications de client qu’un événement s’est produite dans l’objet form.  <br/> |
|[IMAPIViewContext](imapiviewcontextiunknown.md) <br/> |Utilisé pour répondre à des commandes Delete, précédent et suivant dans l’objet form.  <br/> |
|[IPersistMessage](ipersistmessageiunknown.md) <br/> |Utilisé pour enregistrer, initialiser et charger des objets de formulaire vers et depuis le stockage des messages.  <br/> |
   
Pour plus d’informations sur les méthodes des interfaces de formulaire MAPI, voir la documentation de ces interfaces. Vous n’êtes pas obligé de toutes les interfaces de formulaire MAPI implémenter afin de créer un formulaire personnalisé. Un formulaire proprement dite nécessite uniquement que vous implémentez **IPersistMessage**, **IMAPIForm**, et les interfaces **IMAPIFormAdviseSink** . En outre, il est également conseillé de mettre en œuvre **IMAPIFormFactory** et **IMAPIFormInfo**. **IMAPIFormFactory** est utile pour la conformité OLE et **IMAPIFormInfo** permet aux applications clientes bien écrites utilisent plus efficacement vos formulaires. 
  
> [!NOTE]
> En principe, **IMAPIFormAdviseSink** est une interface facultative. Toutefois, il est fortement recommandé d’implémenter dans vos serveurs de formulaire. Cette interface est essentielle pour une interaction efficace entre les clients de messagerie et les serveurs de formulaire, en particulier lorsque plusieurs messages du votre serveur formulaire classe de message sont traitées. 
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

