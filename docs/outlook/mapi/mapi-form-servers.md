---
title: Serveurs de formulaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 855292b8-028e-4c1e-87ed-3f20b9ba584a
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 3c95f6a1d4d50dd6552c6e786d17c40da14f3f3c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351484"
---
# <a name="mapi-form-servers"></a>Serveurs de formulaires MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Du point de vue de l'utilisateur, un formulaire est généralement une feuille des propriétés d'un message ou d'un formulaire de saisie de données qui permet aux utilisateurs d'entrer des informations structurées. Toutefois, il peut s'agir de n'importe quelle interface utilisateur associée à une classe de message. Du point de vue du programmeur, un formulaire se compose des éléments suivants:
  
- Type de message MAPI avec sa propre classe de message et identificateur OLE.
    
- Fichier exécutable qui implémente le serveur de formulaires.
    
- Collection de propriétés MAPI (personnalisé ou autre) utilisée par le serveur de formulaire. Une partie ou la totalité de ces éléments peut être disponible pour les clients de messagerie en vue de leur utilisation.
    
- Fichier de configuration qui décrit le formulaire et utilisé par le gestionnaire de formulaires.
    
Étant donné que les formulaires sont des objets [IMessage](imessageimapiprop.md) , ils présentent des propriétés et un comportement cohérent avec les objets Message MAPI. Toutefois, étant donné que les formulaires peuvent avoir des propriétés personnalisées, des contrôles et un rendu d'affichage propre à l'application, les interfaces MAPI utilisées par les formulaires sont suffisamment génériques pour permettre toute sorte d'interface nécessaire. La définition réelle d'un formulaire est stockée dans une bibliothèque de formulaires, qui est décrite plus loin dans cette section. 
  
> [!NOTE]
> Plus précisément, tous les messages sont des instances de formulaires MAPI. Toutefois, il est généralement plus facile de considérer les formulaires personnalisés comme des cas particuliers de messages, car les formulaires de composition et de lecture de messages électroniques classiques sont les formulaires les plus fréquemment utilisés. Le fait que tous les messages sont réellement des formulaires donne aux formulaires personnalisés le même statut que tout autre message dans le système MAPI. 
  
Chaque formulaire dispose d'un ensemble de propriétés, dont certaines sont visibles dans l'interface utilisateur du formulaire. En règle générale, les propriétés sont mises en correspondance avec les champs de l'interface utilisateur du formulaire. Par exemple, un formulaire de bon de commande peut avoir les champs Item, description, Price, Tax et subTotal. Ces champs sont simplement des rendus visuels des propriétés de formulaire portant le même nom. Les clients déterminent les propriétés prises en charge par une classe de message particulière par le biais de la méthode [IMAPIFormInfo:: CalcFormPropSet](imapiforminfo-calcformpropset.md) , qui est implémentée par le gestionnaire de formulaires MAPI. 
  
Comme les messages de base, les formulaires MAPI peuvent contenir toutes les propriétés de message standard telles que l'expéditeur, le destinataire prévu et le moment où le message a été envoyé. Les formulaires peuvent également contenir un nombre quelconque de propriétés personnalisées spécifiques au formulaire. Par exemple, un formulaire «rapport de bogue» peut contenir des propriétés personnalisées pour le type de bogue, la gravité des bogues et la version du produit.
  
Pour créer un formulaire, vous devez implémenter un serveur de formulaire. Le serveur de formulaire est le fichier exécutable qui est chargé lorsqu'un client de messagerie doit afficher un message qui est le type pris en charge par le serveur de formulaire. Le serveur de formulaires crée à son tour des objets de formulaire, si nécessaire, pour afficher des messages spécifiques et gérer les interactions des utilisateurs avec ces messages.
  
Un fichier de configuration est associé à chaque serveur de formulaire. Ce fichier contient des informations qui décrivent le serveur de formulaire au profit du gestionnaire de formulaires. Le gestionnaire de formulaires utilise ces informations lors de l'installation du serveur de formulaires dans une bibliothèque de formulaires.
  
Pour plus d'informations sur la création des parties d'un formulaire, voir [developING MAPI Form Servers](developing-mapi-form-servers.md).
  
Les serveurs de formulaires adhèrent au modèle COM (Component Object Model). Les serveurs de formulaires s'exécutent en tant que fichiers exécutables autonomes, et non en tant que serveurs in-process. Pour plus d'informations, reportez-vous à la section COM and ActiveX Object Services du kit de développement logiciel Windows.
  
Un identificateur de classe unique (CLSID) identifie chaque serveur de formulaire. Il y a toujours un mappage un-à-un entre un identificateur de classe et sa classe de message. Toutefois, cela ne signifie pas qu'un serveur de formulaire ne peut fonctionner qu'avec des messages d'une seule classe de message. Si aucun serveur de formulaires n'est disponible pour traiter un message d'une classe particulière, le gestionnaire de formulaires utilisé doit tenter de trouver un serveur de formulaire pour une classe de message plus haut dans la hiérarchie de la classe de message; le gestionnaire de formulaires par défaut fourni avec le kit de développement logiciel Windows effectue cette opération. Ce type de serveur de formulaire ne pourra probablement afficher qu'un sous-ensemble des propriétés du message (celles prises en charge par la superclasse), mais il sera préférable de ne rien faire. Que se passe-t-il si aucun serveur de formulaire correspondant n'est trouvé, il s'agit d'un détail d'implémentation spécifique au gestionnaire de formulaires qui est utilisé; le gestionnaire de formulaires par défaut n'ouvre pas les messages lorsque cela se produit.
  
Pour plus d'informations, consultez la rubrique [MAPI message classes](mapi-message-classes.md).
  
## <a name="see-also"></a>Voir aussi



[Formulaires MAPI](mapi-forms.md)

