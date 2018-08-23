---
title: Stockage de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ddf9158-3c10-408a-aeaf-5a382c4339e7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c98427ab326ada0b717282dc4077d526780aa45c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568160"
---
# <a name="form-storage"></a>Stockage de formulaire

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Bien qu’il n’est pas nécessaire de connaître tous les détails de la façon dont les formulaires sont stockés physiquement, il est utile de comprendre certains des concepts principaux. Par conséquent, avant de décrire les trois types de bibliothèques de formulaires pris en charge par le Gestionnaire de formulaire par défaut, cette rubrique fournit une vue d’ensemble de la façon dont les formulaires sont stockés.
  
Définitions de formulaire peuvent être physiquement stockées dans des dossiers d’un ou plusieurs magasins de message MAPI. Chaque dossier MAPI peut être considéré comme ayant deux zones pour le stockage des objets de message : le composant standard et le composant associé. Le composant standard du dossier inclut les messages et les dossiers qui manipulent des utilisateurs.
  
Le composant associé inclut des objets de message masqué qui sont associés au dossier, y compris les définitions de formulaire, les affichages, les modèles de règle, des modèles de réponse et ainsi de suite. Ce composant de substitution est appelé la table de contenu associées au dossier et l’ensemble des messages dans le tableau contenu associé est appelé les informations associées au dossier. Les messages masqués font partie intégrante du dossier et sont copiés ainsi que le contenu du dossier standard lorsque le dossier est copié. Bien que physiquement stockées sous forme de messages, les informations de table de contenu associé d’un dossier se comportement plus comme propriétés que comme messages visibles. N’importe quel objet folder qui prend en charge un tableau contenu associé est capable de stocker des formulaires personnalisés. La méthode [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) peut retourner le contenu standard ou le contenu du dossier, selon la valeur de paramètre de la méthode _ulflags_ associé. 
  
Une bibliothèque de formulaires se compose des définitions de formulaire stockées dans la table de contenu associé d’un dossier. La définition de formulaire comprend les propriétés du formulaire, les actions de formulaire prend en charge et même le formulaire fichier exécutable server, qui est stocké comme une ou plusieurs pièces jointes des messages.
  
De plus, les formulaires peuvent être stockées dans un fichier ou l’emplacement du Gestionnaire de formulaire utilisé prend en charge. Le Gestionnaire de formulaire par défaut stocke des serveurs de formulaire dans des dossiers MAPI, mais un gestionnaire de formulaire personnalisé peut implémenter sa propre stockage pour les serveurs de formulaire.
  
Un formulaire peut avoir plusieurs interfaces utilisateur liées à sa classe de message. Par exemple, un formulaire peut avoir des interfaces utilisateur en lecture et de composition distinctes. Le formulaire prend en charge de l’appel de l’interface utilisateur appropriés pour les demandes utilisateur différent, en fonction de laquelle des verbes du formulaire est appelée. Par exemple, si votre serveur de formulaire a composition distincte et la lecture des interfaces utilisateur, l’interface utilisateur de composition peut être ouverts automatiquement lorsque l’utilisateur crée un nouveau message de classe de message du formulaire et l’interface utilisateur de lecture peut être ouverts automatiquement lorsque le utilisateur ouvre un message existant de la classe de message du formulaire.
  
La plupart des informations stockées dans une définition de formulaire est disponible en appelant la méthode [IMAPIFormInfo::IMAPIProp](imapiforminfoimapiprop.md) sur un objet **IMAPIFormInfo** . L’interface **IMAPIFormInfo** simplifie l’accès aux informations d’un formulaire en appelant tous les dossiers MAPI et méthodes nécessaires pour récupérer les informations de message. Un objet **IMAPIFormInfo** peut être obtenu en appelant la méthode [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) . 
  
Les trois types de bibliothèques de formulaires sont décrits dans les rubriques [Local bibliothèques de formulaires](local-form-libraries.md), [Les bibliothèques de formulaires de dossier](folder-form-libraries.md) et [Les bibliothèques de formulaires personnels](personal-form-libraries.md).
  
## <a name="see-also"></a>Voir aussi

- [Formulaires MAPI](mapi-forms.md)

