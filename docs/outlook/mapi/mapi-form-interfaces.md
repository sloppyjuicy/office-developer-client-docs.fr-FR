---
title: Interfaces de formulaire MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f207f9550c61ad69fd1fc560cdb2084b7bb56c6f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412344"
---
# <a name="mapi-form-interfaces"></a>Interfaces de formulaire MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI définit les interfaces suivantes relatives aux formulaires.
  
|**Nom de l’interface**|**Description**|
|:-----|:-----|
|[IMAPIForm](imapiformiunknown.md) <br/> |Manipule les objets de formulaire et gère les commandes d’objet de formulaire.  <br/> |
|[IMAPIFormAdviseSink](imapiformadvisesinkiunknown.md) <br/> |Détermine si l’objet de formulaire peut gérer le message suivant et modifie l’état suivant ou précédent de l’objet de formulaire.  <br/> |
|[IMAPIFormContainer](imapiformcontaineriunknown.md) <br/> |Prend en charge l’installation, la désinstallation et la résolution des serveurs de formulaires par rapport à un conteneur de formulaire spécifique.  <br/> |
|[IMAPIFormFactory](imapiformfactoryiunknown.md) <br/> |Prend en charge l’utilisation de serveurs de formulaires configurables au moment de l’utilisation.  <br/> |
|[IMAPIFormInfo](imapiforminfoimapiprop.md) <br/> |Permet aux applications clientes de fonctionner avec des propriétés spécifiques à une classe de message.  <br/> |
|[IMAPIFormMgr](imapiformmgriunknown.md) <br/> |Permet aux applications clientes d’obtenir des informations sur les serveurs de formulaires, d’activer les serveurs de formulaires et d’installer des serveurs de formulaires dans le système de messagerie.  <br/> |
|[IMAPIMessageSite](imapimessagesiteiunknown.md) <br/> |Permet de manipuler des messages associés à des objets de formulaire.  <br/> |
|[IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) <br/> |Avertit les applications clientes qu’un événement s’est produit dans l’objet formulaire.  <br/> |
|[IMAPIViewContext](imapiviewcontextiunknown.md) <br/> |Permet de répondre aux commandes Next, Previous et Delete dans l’objet de formulaire.  <br/> |
|[IPersistMessage](ipersistmessageiunknown.md) <br/> |Permet d’enregistrer, d’initialiser et de charger des objets de formulaire vers et depuis le stockage des messages.  <br/> |
   
Pour plus d’informations sur les méthodes des interfaces de formulaire MAPI, voir la documentation de ces interfaces. Vous n’avez pas besoin d’implémenter toutes les interfaces de formulaire MAPI pour créer un formulaire personnalisé. Un formulaire lui-même nécessite uniquement que vous implémentiez les interfaces **IPersistMessage,** **IMAPIForm** et **IMAPIFormAdviseSink.** En outre, il est également bon d’implémenter **IMAPIFormFactory** et **IMAPIFormInfo**. **IMAPIFormFactory** est utile pour la conformité OLE, et **IMAPIFormInfo** permet aux applications clientes bien écrites de mieux utiliser vos formulaires. 
  
> [!NOTE]
> À proprement parler, **IMAPIFormAdviseSink** est une interface facultative. Toutefois, il est vivement recommandé de l’implémenter sur vos serveurs de formulaires. Cette interface est essentielle pour une interaction efficace entre les clients de messagerie et les serveurs de formulaires, en particulier lorsque plusieurs messages de la classe de message de votre serveur de formulaires sont traités. 
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

