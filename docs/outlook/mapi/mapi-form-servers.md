---
title: Serveurs de formulaire MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 855292b8-028e-4c1e-87ed-3f20b9ba584a
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: dad36bfc5fed296cff3baa4cc11bb1fdf359c45a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784615"
---
# <a name="mapi-form-servers"></a>Serveurs de formulaire MAPI

  
  
**S’applique à**: Outlook 
  
Point de vue de l’utilisateur, d’un formulaire est généralement une feuille de propriétés pour un message ou un formulaire de saisie de données qui permet aux utilisateurs d’entrer des informations structurées. Toutefois, il peut être une interface utilisateur qui est associée à une classe de message. À partir du point de vue du programmeur, un formulaire se compose de :
  
- Type de message MAPI avec son propre classe de message et l’identificateur OLE.
    
- Le fichier exécutable qui implémente le serveur du formulaire.
    
- Une collection de propriétés MAPI — personnalisé ou dans le cas contraire, qui utilise le serveur de formulaire. Certains ou tous ces peuvent être disponible pour les clients de messagerie à utiliser.
    
- Le fichier de configuration qui décrit le formulaire et est utilisé par le Gestionnaire de formulaire.
    
Étant donné que les formulaires sont des objets [IMessage](imessageimapiprop.md) , elles présentent les propriétés et le comportement est cohérent avec les objets de message MAPI. Toutefois, étant donné que les formulaires peuvent avoir un affichage rendu qui est spécifique à l’application, les contrôles et les propriétés personnalisées, les interfaces MAPI qui constitue l’utilisation sont suffisamment génériques pour permettre de tout type d’interface qui est nécessaire. La définition d’un formulaire est stockée dans une bibliothèque de formulaires, voir plus loin dans cette section. 
  
> [!NOTE]
> Plus précisément, tous les messages sont des instances de formulaires MAPI. Toutefois, il est généralement plus facile de considérer les formulaires personnalisés comme cas particuliers de messages, depuis les formulaires de composition et lecture des messages électroniques par défaut sont les plus couramment utilisés forms. Le fait que tous les messages sont simplement les permet de formulaires personnalisés forms le même statut que tous les messages dans le système MAPI. 
  
Chaque formulaire dispose d’un ensemble de propriétés, dont certains sont visibles dans l’interface utilisateur du formulaire. En règle générale, les propriétés correspondent aux champs dans l’interface utilisateur du formulaire. Par exemple, un bon de commande peut avoir les champs d’élément, Description, prix, taxe et sous-total. Ces champs sont rendus visual simplement des propriétés de formulaire du même nom. Clients concernées les propriétés qui sont prises en charge par une classe de message particulier par le biais de la méthode [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md) , qui est implémentée par le Gestionnaire de formulaire MAPI. 
  
Comme les messages de base, formulaires MAPI peuvent contenir toutes les propriétés de message standard telles que l’expéditeur, destinataire, et lorsque le message a été envoyé. Formulaires peuvent également contenir n’importe quel nombre de propriétés personnalisées qui sont spécifiques à l’écran. Par exemple un formulaire « Rapport de bogue » peut contenir des propriétés personnalisées de Type bogue, gravité des bogues et Version du produit.
  
Pour créer un formulaire, vous devez implémenter un serveur de formulaire. Le serveur de formulaire est le fichier exécutable qui est chargé lorsqu’un client de messagerie a besoin afficher un message qui est le type pris en charge par le serveur de formulaire. Le serveur de formulaire crée à son tour des objets de formulaire que nécessaire pour afficher des messages spécifiques et gérer les interactions des utilisateurs avec ces messages.
  
Chaque serveur du formulaire est associé à un fichier de configuration. Ce fichier contient des informations décrivant le serveur formulaire inscrivent dans le cadre du Gestionnaire de formulaire. Le Gestionnaire de formulaire utilise ces informations lorsque vous installez le serveur de formulaire dans une bibliothèque de formulaires.
  
Pour plus d’informations sur la création des composants d’un formulaire, voir [Développement de serveurs de formulaire MAPI](developing-mapi-form-servers.md).
  
Serveurs de formulaire sont conformes à l’objet COM (Component Model). Serveurs de formulaire exécuter en tant qu’exécutables autonomes, pas en tant que serveurs in-process. Pour plus d’informations, consultez la section COM et ActiveX Object Services dans le SDK de Windows.
  
Un identificateur unique de classe (CLSID) identifie chaque serveur du formulaire. Il y a toujours une correspondance directe entre un identificateur de classe et de sa classe de message. Cela ne signifie pas, toutefois, qu’un serveur de formulaire peut ne fonctionnent qu’avec des messages d’une classe de message. Si aucun serveur de formulaire n’est disponible pour un message d’une classe spécifique de service, le Gestionnaire de formulaire utilisé doit essayer de trouver un serveur de formulaire pour une classe de message dans la hiérarchie de classe de message ; le Gestionnaire de formulaire par défaut fourni avec le Kit de développement Windows effectue cette action. Ce type de serveur formulaire sera probablement en mesure d’afficher uniquement un sous-ensemble des propriétés du message (ceux pris en charge par la superclasse), mais il ne sera pas toujours mieux que rien. Que se passe-t-il lorsque aucun serveur formulaire est trouvé tout est un détail d’implémentation spécifique au Gestionnaire de formulaire utilisé ; le Gestionnaire de formulaire par défaut n’ouvre pas les messages dans ce cas.
  
Pour plus d’informations, consultez [Classes de Message MAPI](mapi-message-classes.md).
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

