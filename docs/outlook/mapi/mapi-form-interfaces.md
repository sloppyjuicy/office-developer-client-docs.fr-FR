---
title: Interfaces de formulaire MAPI
description: Cet article fournit des liens et des descriptions vers les différentes interfaces et méthodes de formulaire MAPI avec des notes supplémentaires.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
ms.openlocfilehash: 4c7f1012328c315760b20f28855ce5d54e345039
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815729"
---
# <a name="mapi-form-interfaces"></a>Interfaces de formulaire MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI définit les interfaces suivantes relatives aux formulaires.
  
|**Nom de l’interface**|**Description**|
|:-----|:-----|
|[IMAPIForm](imapiformiunknown.md) <br/> |Manipule les objets de formulaire et gère les commandes d’objet de formulaire. |
|[IMAPIFormAdviseSink](imapiformadvisesinkiunknown.md) <br/> |Détermine si l’objet de formulaire peut gérer le message suivant et modifie l’état suivant ou précédent de l’objet de formulaire. |
|[IMAPIFormContainer](imapiformcontaineriunknown.md) <br/> |Prend en charge l’installation, la désinstallation et la résolution de serveurs de formulaires sur un conteneur de formulaires spécifique. |
|[IMAPIFormFactory](imapiformfactoryiunknown.md) <br/> |Prend en charge l’utilisation de serveurs de formulaires d’exécution configurables. |
|[IMAPIFormInfo](imapiforminfoimapiprop.md) <br/> |Permet aux applications clientes d’utiliser des propriétés spécifiques à une classe de message. |
|[IMAPIFormMgr](imapiformmgriunknown.md) <br/> |Permet aux applications clientes d’obtenir des informations sur les serveurs de formulaires, d’activer les serveurs de formulaires et d’installer des serveurs de formulaires dans le système de messagerie. |
|[IMAPIMessageSite](imapimessagesiteiunknown.md) <br/> |Utilisé pour manipuler les messages associés aux objets de formulaire. |
|[IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) <br/> |Avertit les applications clientes qu’un événement s’est produit dans l’objet de formulaire. |
|[IMAPIViewContext](imapiviewcontextiunknown.md) <br/> |Utilisé pour répondre aux commandes Suivant, Précédent et Supprimer dans l’objet de formulaire. |
|[IPersistMessage](ipersistmessageiunknown.md) <br/> |Permet d’enregistrer, d’initialiser et de charger des objets de formulaire vers et depuis le stockage de messages. |
   
Pour plus d’informations sur les méthodes des interfaces de formulaire MAPI, consultez la documentation de ces interfaces. Vous n’avez pas besoin d’implémenter toutes les interfaces de formulaire MAPI pour créer un formulaire personnalisé. Un formulaire lui-même nécessite uniquement que vous implémentez les **interfaces IPersistMessage**, **IMAPIForm** et **IMAPIFormAdviseSink** . En outre, il est également judicieux d’implémenter **IMAPIFormFactory** et **IMAPIFormInfo**. **IMAPIFormFactory** est utile pour la conformité OLE, et **IMAPIFormInfo** permet aux applications clientes bien écrites de mieux utiliser vos formulaires. 
  
> [!NOTE]
> À proprement parler, **IMAPIFormAdviseSink** est une interface facultative. Toutefois, il est fortement recommandé de l’implémenter dans vos serveurs de formulaires. Cette interface est essentielle pour une interaction efficace entre les clients de messagerie et les serveurs de formulaires, en particulier lorsque plusieurs messages de la classe de message de votre serveur de formulaire sont traités. 
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

