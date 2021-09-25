---
title: Serveurs de formulaire MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 855292b8-028e-4c1e-87ed-3f20b9ba584a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 10c71c9cebcc66542846c0631be31d6a893d82f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561241"
---
# <a name="mapi-form-servers"></a>Serveurs de formulaire MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Du point de vue de l’utilisateur, un formulaire est généralement une feuille de propriétés pour un message ou un formulaire de saisie de données qui permet aux utilisateurs d’entrer des informations structurées. Toutefois, il peut s’agit de n’importe quelle interface utilisateur associée à une classe de message. Du point de vue du programmeur, un formulaire se compose des points de vue ci-après :
  
- Type de message MAPI avec sa propre classe de message et son identificateur OLE.
    
- Fichier exécutable qui implémente le serveur de formulaires.
    
- Collection de propriétés MAPI (personnalisées ou autres) que le serveur de formulaires utilise. Une partie ou l’ensemble de ces éléments peuvent être disponibles pour une utilisation par les clients de messagerie.
    
- Fichier de configuration qui décrit le formulaire et est utilisé par le gestionnaire de formulaires.
    
Étant donné que les formulaires sont des objets [IMessage,](imessageimapiprop.md) ils présentent des propriétés et un comportement cohérents avec les objets de message MAPI. Toutefois, étant donné que les formulaires peuvent avoir des propriétés personnalisées, des contrôles et un rendu d’affichage propre à l’application, les interfaces MAPI que les formulaires utilisent sont suffisamment génériques pour permettre tout type d’interface nécessaire. La définition réelle d’un formulaire est stockée dans une bibliothèque de formulaires, comme expliqué plus loin dans cette section. 
  
> [!NOTE]
> Plus précisément, tous les messages sont des instances de formulaires MAPI. Toutefois, il est généralement plus facile de voir les formulaires personnalisés comme des cas particuliers de messages, car les formulaires de composition et de lecture de messages électroniques classiques sont les formulaires les plus couramment utilisés. Le fait que tous les messages soient simplement des formulaires donne aux formulaires personnalisés le même état que tout autre message dans le système MAPI. 
  
Chaque formulaire possède un ensemble de propriétés, dont certaines sont visibles dans l’interface utilisateur du formulaire. En règle générale, les propriétés sont en correspondance avec les champs de l’interface utilisateur du formulaire. Par exemple, un bon de commande peut avoir les champs Item, Description, Price, Tax et Subtotal. Ces champs sont simplement des rendus visuels des propriétés de formulaire des mêmes noms. Les clients peuvent déterminer quelles propriétés sont pris en charge par une classe de message particulière via la méthode [IMAPIFormInfo::CalcFormPropSet,](imapiforminfo-calcformpropset.md) qui est implémentée par le gestionnaire de formulaire MAPI. 
  
Comme les messages de base, les formulaires MAPI peuvent contenir toutes les propriétés de message standard telles que l’expéditeur, le destinataire prévu et le moment où le message a été envoyé. Les formulaires peuvent également contenir n’importe quel nombre de propriétés personnalisées spécifiques au formulaire. Par exemple, un formulaire « Rapport de bogue » peut contenir des propriétés personnalisées pour le type de bogue, la gravité du bogue et la version du produit.
  
Pour créer un formulaire, vous devez implémenter un serveur de formulaires. Le serveur de formulaires est le fichier exécutable qui est chargé lorsqu’un client de messagerie doit afficher un message qui est le type pris en charge par le serveur de formulaires. Le serveur de formulaire crée à son tour des objets de formulaire si nécessaire pour afficher des messages spécifiques et gérer les interactions utilisateur avec ces messages.
  
Un fichier de configuration est associé à chaque serveur de formulaire. Ce fichier contient des informations qui décrivent le serveur de formulaires pour l’avantage du gestionnaire de formulaires. Le gestionnaire de formulaires utilise ces informations lors de l’installation du serveur de formulaires dans une bibliothèque de formulaires.
  
Pour plus d’informations sur la création des composants d’un formulaire, voir [Developing MAPI Form Servers](developing-mapi-form-servers.md).
  
Les serveurs de formulaire adhèrent au modèle objet composant (COM). Les serveurs de formulaire s’exécutent en tant qu’exécutables autonomes, et non en tant que serveurs in-proc. Pour plus d’informations, voir la section COM et ActiveX Services d’objets dans Windows SDK.
  
Un identificateur de classe unique (CLSID) identifie chaque serveur de formulaires. Il existe toujours un mappage un-à-un entre un identificateur de classe et sa classe de message. Toutefois, cela ne signifie pas qu’un serveur de formulaires ne peut fonctionner qu’avec les messages d’une classe de message. Si aucun serveur de formulaire n’est disponible pour le service d’un message d’une classe particulière, le gestionnaire de formulaires utilisé doit tenter de trouver un serveur de formulaire pour une classe de message supérieure dans la hiérarchie des classes de message . Le gestionnaire de formulaires par défaut fourni avec Windows SDK le fait. Un tel serveur de formulaires sera probablement en mesure de restituer uniquement un sous-ensemble des propriétés du message (celles qui sont pris en charge par la superclasse), mais il sera préférable à rien. Ce qui se produit lorsqu’aucun serveur de formulaire correspondant n’est trouvé, c’est un détail d’implémentation spécifique au gestionnaire de formulaires utilisé . Le gestionnaire de formulaires par défaut n’ouvre pas les messages lorsque cela se produit.
  
Pour plus d’informations, voir [CLASSES de message MAPI.](mapi-message-classes.md)
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

