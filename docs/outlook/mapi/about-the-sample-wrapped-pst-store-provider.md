---
title: À propos de l’exemple de fournisseur de magasins PST wrapped
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 953391ce-31a2-3271-365a-284cf5e15d82
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: 779dd96c4f07c0c5eee60ae046cd17db98eebfd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432722"
---
# <a name="about-the-sample-wrapped-pst-store-provider"></a>À propos de l’exemple de fournisseur de magasins PST wrapped

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
## <a name="overview-of-message-store-providers"></a>Vue d’ensemble des fournisseurs de magasins de messages

Les fournisseurs de magasins de messages gèrent le stockage et la récupération des messages et d’autres informations pour les utilisateurs d’applications clientes. Les informations de message sont organisées à l’aide d’un système hiérarchique appelé magasin de messages. La magasin de messages est implémentée dans plusieurs niveaux, avec des conteneurs appelés dossiers contenant des messages de différents types. Il n’existe aucune limite au nombre de niveaux dans une magasin de messages ; peuvent contenir de nombreux sous-dossiers.
  
Les données de la boutique de messages peuvent être utilisées de différentes manières. Outre l’utilisation classique de la messagerie électronique, les dossiers peuvent être utilisés comme forum de discussion publique, comme référentiel pour les documents de référence ou comme conteneur pour les informations de forum. Une seule magasin de messages peut contenir de nombreux types d’informations, dont certains peuvent être modifiables et d’autres non. Plusieurs clients peuvent installer la même magasin de messages, ce qui permet de partager facilement et rapidement des données.
  
Les dossiers de la boutique de messages vous permettent de trier et de filtrer des messages et de personnaliser l’affichage dans un affichage d’interface utilisateur. Les liens vers les messages filtrés sont placés dans des dossiers spéciaux appelés dossiers de résultats de recherche. L’utilisateur d’une application cliente entre des critères de filtrage, que MAPI appelle une restriction, et les critères sont appliqués aux messages stockés dans un ou plusieurs dossiers. Par exemple, un utilisateur peut vouloir afficher uniquement les messages traitant d’un sujet particulier avec des dates d’arrivée plus récentes que la semaine dernière. Les références aux messages qui correspondent aux critères sont répertoriées dans le dossier des résultats de recherche et les messages réels restent dans leurs dossiers habituels.
  
Les messages sont les unités de données transférées d’un utilisateur ou d’une application vers un autre utilisateur ou une autre application. Chaque message contient des informations sur le texte et l’enveloppe de message utilisées pour la transmission. Certains messages incluent une ou plusieurs pièces jointes, ou des données supplémentaires liées à un message et transporté avec celui-ci sous la forme d’un fichier, d’un autre message ou d’un objet OLE.
  
## <a name="the-sample-wrapped-pst-store-provider"></a>Exemple de fournisseur de magasins PST wrapped

L’API de réplication vous permet de répliquer des éléments à partir d’un référentiel de données back end dans Outlook magasin PST. Vous utilisez l’API de réplication pour répliquer les données dans un magasin PST dédié et suivre l’état de synchronisation. Cette approche ne nécessite pas l’introduction d’un fournisseur de magasin MAPI personnalisé, qui est complexe à écrire et à gérer. Toutefois, le fournisseur de magasin PST doit être wrapped pour fonctionner avec l’API de réplication.
  
L’exemple de fournisseur de magasins PST wrapped utilise le fournisseur de fichiers de dossiers personnels (PST) comme système de stockage des données. Le fournisseur de magasin PST wrapped doit être utilisé conjointement avec l’API de réplication. Pour plus d’informations, voir [à propos de l’API de réplication.](about-the-replication-api.md) La plupart des fonctions dans l’exemple de fournisseur de magasin PST Wrapped passent leurs arguments directement au fournisseur PST sous-jacent. Certaines fonctions nécessitent une implémentation spéciale et sont décrites dans les rubriques suivantes.
  
## <a name="in-this-section"></a>Dans cette section

- [Installation de l’exemple de fournisseur de magasin PST Wrapped](installing-the-sample-wrapped-pst-store-provider.md)
    
- Explique comment télécharger et installer l’exemple de fournisseur de magasin PST Wrapped.
    
- [Initialisation d’un fournisseur de magasin PST wrapped](initializing-a-wrapped-pst-store-provider.md)
    
- La première étape de l’implémentation d’un fournisseur de magasin PST wrapped consiste à initialiser et configurer le fournisseur de magasin PST wrapped.
    
- [Connexion à un fournisseur de magasin PST wrapped](logging-on-to-a-wrapped-pst-store-provider.md)
    
- Après l’initialisation d’un fournisseur de magasins PST wrapped, vous devez implémenter des fonctions afin que MAPI et lepooler MAPI se connectent au fournisseur de magasin PST wrapped.
    
- [Utilisation d’un fournisseur de magasin PST wrapped](using-a-wrapped-pst-store-provider.md)
    
- Pour utiliser un fournisseur de magasin PST encapsulé, vous devez encapsuler l’interface **[IMAPISupport::IUnknown](imapisupportiunknown.md)** pour implémenter des tâches courantes de fournisseur de magasin PST encapsulé. 
    
- [Arrêt d’un fournisseur de magasin PST wrapped](shutting-down-a-wrapped-pst-store-provider.md)
    
- Une fois que vous avez terminé d’utiliser un fournisseur de magasin PST wrapped, vous devez arrêter correctement le fournisseur de magasin PST wrapped.
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[D�veloppement d'un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

