---
title: À propos de l'exemple de fournisseur de banque d'informations PST encapsulé
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 953391ce-31a2-3271-365a-284cf5e15d82
description: 'Dernière modification: 03 juillet 2012'
ms.openlocfilehash: 779dd96c4f07c0c5eee60ae046cd17db98eebfd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432722"
---
# <a name="about-the-sample-wrapped-pst-store-provider"></a>À propos de l'exemple de fournisseur de banque d'informations PST encapsulé

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
## <a name="overview-of-message-store-providers"></a>Vue d'ensemble des fournisseurs de banques de messages

Les fournisseurs de banques de messages gèrent le stockage et l'extraction des messages et d'autres informations pour les utilisateurs des applications clientes. Les informations du message sont organisées à l'aide d'un système hiérarchique appelé Banque de messages. La Banque de messages est implémentée à plusieurs niveaux, avec des conteneurs appelés dossiers qui contiennent des messages de types différents. Il n'y a pas de limite au nombre de niveaux dans une banque de messages; les dossiers peuvent contenir de nombreux sous-dossiers.
  
Les données de banque de messages peuvent être utilisées de différentes manières. En plus de l'utilisation de la messagerie par défaut, les dossiers peuvent être utilisés comme un forum de discussion public, comme référentiel pour des documents de référence ou comme conteneur pour les informations du forum électronique. Un seul magasin de messages peut contenir de nombreux types d'informations, dont certains sont modifiables et d'autres non. Plusieurs clients peuvent installer le même magasin de messages, ce qui vous permet de partager facilement et rapidement les données.
  
Les dossiers de banque de messages vous permettent de trier et de filtrer des messages et de personnaliser l'affichage dans une interface utilisateur (IU). Les liens vers les messages filtrés sont conservés dans des dossiers spéciaux appelés dossiers de résultats de recherche. L'utilisateur d'une application cliente entre les critères de filtrage auxquels MAPI fait référence en tant que restriction, et les critères sont appliqués aux messages stockés dans un ou plusieurs dossiers. Par exemple, un utilisateur peut souhaiter afficher uniquement les messages traitant d'un objet particulier dont les dates d'arrivée sont postérieures à la semaine dernière. Les références aux messages qui répondent aux critères sont répertoriées dans le dossier Search-Results et les véritables messages restent dans leurs dossiers ordinaires.
  
Les messages sont les unités de données transférées à partir d'un utilisateur ou d'une application vers un autre utilisateur ou une autre application. Chaque message contient un texte de message et des informations d'enveloppe de message qui sont utilisées pour la transmission. Certains messages incluent une ou plusieurs pièces jointes, ou des données supplémentaires liées à un message et transportées avec un message sous la forme d'un fichier, d'un autre message ou d'un objet OLE.
  
## <a name="the-sample-wrapped-pst-store-provider"></a>Exemple de fournisseur de banque de fichiers PST encapsulée

L'API de réPlication vous permet de répliquer des éléments à partir d'un référentiel de données principal dans un magasin Outlook PST. L'API de réPlication permet de répliquer les données dans un magasin PST dédié et de suivre l'état de synchronisation. Cette approche ne nécessite pas l'introduction d'un fournisseur de magasins MAPI personnalisé, ce qui est complexe à écrire et à gérer. Toutefois, le fournisseur de banque PST doit être encapsulé pour fonctionner avec l'API de réPlication.
  
L'exemple de fournisseur de banque d'informations PST encapsulé utilise le fournisseur de fichiers de dossiers personnels (PST) comme serveur principal pour le stockage des données. Le fournisseur de magasins PST encapsulé doit être utilisé conjointement avec l'API de réPlication. Pour plus d'informations, consultez [la rubrique à propos de l'API](about-the-replication-api.md)de réplication. La plupart des fonctions dans l'exemple de fournisseur de magasins PST encapsulé passent leurs arguments directement au fournisseur PST sous-jacent. Certaines fonctions nécessitent une implémentation spéciale et sont décrites dans les rubriques suivantes.
  
## <a name="in-this-section"></a>Dans cette section

- [Installation de l'exemple de fournisseur de magasins PST encapsulé](installing-the-sample-wrapped-pst-store-provider.md)
    
- Explique comment télécharger et installer l'exemple de fournisseur de banque d'informations PST encapsulé.
    
- [Initialisation d'un fournisseur de magasins PST encapsulé](initializing-a-wrapped-pst-store-provider.md)
    
- La première étape de l'implémentation d'un fournisseur de magasins PST encapsulé consiste à initialiser et configurer le fournisseur de magasins PST encapsulé.
    
- [Connexion à un fournisseur de magasins PST encapsulé](logging-on-to-a-wrapped-pst-store-provider.md)
    
- Après l'initialisation d'un fournisseur de magasins PST encapsulé, vous devez implémenter des fonctions afin que MAPI et le spouleur MAPI puissent se connecter au fournisseur de magasins PST encapsulé.
    
- [Utilisation d'un fournisseur de magasins PST encapsulé](using-a-wrapped-pst-store-provider.md)
    
- Pour utiliser un fournisseur de magasins PST encapsulé, vous devez encapsuler l'interface **[IMAPISupport:: IUnknown](imapisupportiunknown.md)** pour implémenter les tâches courantes du fournisseur de magasins PST encapsulées. 
    
- [Arrêt d'un fournisseur de magasins PST encapsulé](shutting-down-a-wrapped-pst-store-provider.md)
    
- Une fois que vous avez fini d'utiliser un fournisseur de magasins PST encapsulé, vous devez arrêter correctement le fournisseur de magasins PST encapsulé.
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[D�veloppement d'un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

