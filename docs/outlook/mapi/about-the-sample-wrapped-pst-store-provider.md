---
title: À propos de l’exemple de fournisseur de magasin PST encapsulé
description: Décrit l’exemple de fournisseur de magasin PST encapsulé, qui utilise le fournisseur PST (Personal Folders File) comme serveur principal pour le stockage des données.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 953391ce-31a2-3271-365a-284cf5e15d82
ms.openlocfilehash: 54fde3c4496e789be16d24cd39e323d64e508457
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770130"
---
# <a name="about-the-sample-wrapped-pst-store-provider"></a>À propos de l’exemple de fournisseur de magasin PST encapsulé

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
## <a name="overview-of-message-store-providers"></a>Vue d’ensemble des fournisseurs de magasin de messages

Les fournisseurs de magasins de messages gèrent le stockage et la récupération des messages et d’autres informations pour les utilisateurs des applications clientes. Les informations de message sont organisées à l’aide d’un système hiérarchique appelé magasin de messages. Le magasin de messages est implémenté à plusieurs niveaux, avec des conteneurs appelés dossiers contenant des messages de différents types. Il n’existe aucune limite au nombre de niveaux dans un magasin de messages ; peuvent contenir de nombreux sous-dossiers.
  
Les données du magasin de messages peuvent être utilisées de différentes façons. En plus de l’utilisation classique des e-mails, les dossiers peuvent être utilisés comme forum de discussion publique, comme référentiel pour les documents de référence ou comme conteneur pour les informations du tableau d’affichage. Un magasin de messages unique peut contenir de nombreux types d’informations, certains modifiables et d’autres non. Plusieurs clients peuvent installer le même magasin de messages, ce qui facilite et accélère le partage des données.
  
Les dossiers du magasin de messages vous permettent de trier et de filtrer les messages et de personnaliser l’affichage dans un affichage d’interface utilisateur. Les liens vers les messages filtrés sont conservés dans des dossiers spéciaux appelés dossiers de résultats de recherche. L’utilisateur d’une application cliente entre des critères de filtrage, que MAPI appelle une restriction, et les critères sont appliqués aux messages stockés dans un ou plusieurs dossiers. Par exemple, un utilisateur peut souhaiter afficher uniquement les messages traitant d’un sujet particulier avec des dates d’arrivée plus récentes que la semaine dernière. Les références aux messages qui correspondent aux critères sont répertoriées dans le dossier des résultats de recherche et les messages réels restent dans leurs dossiers standard.
  
Les messages sont les unités de données transférées d’un utilisateur ou d’une application à un autre utilisateur ou application. Chaque message contient des informations de texte et d’enveloppe de message utilisées pour la transmission. Certains messages incluent une ou plusieurs pièces jointes, ou des données supplémentaires liées à un message sous la forme d’un fichier, d’un autre message ou d’un objet OLE.
  
## <a name="the-sample-wrapped-pst-store-provider"></a>Exemple de fournisseur de magasin PST encapsulé

L’API de réplication vous permet de répliquer des éléments d’un référentiel de données back-end dans un magasin PST Outlook. Vous utilisez l’API de réplication pour répliquer les données dans un magasin PST dédié et effectuer le suivi de l’état de synchronisation. Cette approche ne vous oblige pas à introduire un fournisseur de magasin MAPI personnalisé, qui est complexe à écrire et à gérer. Toutefois, le fournisseur du magasin PST doit être encapsulé pour fonctionner avec l’API de réplication.
  
L’exemple de fournisseur de magasin PST encapsulé utilise le fournisseur PST (Personal Folders File) comme serveur principal pour stocker les données. Le fournisseur du magasin PST encapsulé doit être utilisé conjointement avec l’API de réplication. Pour plus d’informations, consultez [À propos de l’API de réplication](about-the-replication-api.md). La plupart des fonctions de l’exemple de fournisseur de magasin PST encapsulé passent leurs arguments directement au fournisseur PST sous-jacent. Certaines fonctions nécessitent une implémentation spéciale et sont décrites dans les rubriques suivantes.
  
## <a name="in-this-section"></a>Contenu de cette section

- [Installation de l’exemple de fournisseur de magasin PST encapsulé](installing-the-sample-wrapped-pst-store-provider.md)
    
- Explique comment télécharger et installer l’exemple de fournisseur de magasin PST encapsulé.
    
- [Initialisation d’un fournisseur de magasin PST encapsulé](initializing-a-wrapped-pst-store-provider.md)
    
- La première étape de l’implémentation d’un fournisseur de magasin PST encapsulé consiste à initialiser et configurer le fournisseur de magasin PST encapsulé.
    
- [Connexion à un fournisseur de magasin PST encapsulé](logging-on-to-a-wrapped-pst-store-provider.md)
    
- Une fois qu’un fournisseur de magasin PST encapsulé est initialisé, vous devez implémenter des fonctions afin que MAPI et le spouleur MAPI puissent se connecter au fournisseur de magasin PST encapsulé.
    
- [Utilisation d’un fournisseur de magasin PST encapsulé](using-a-wrapped-pst-store-provider.md)
    
- Pour utiliser un fournisseur de magasin PST encapsulé, vous devez encapsuler l’interface **[IMAPISupport::IUnknown pour implémenter](imapisupportiunknown.md)** des tâches de fournisseur de magasin PST encapsulées courantes. 
    
- [Arrêt d’un fournisseur de magasin PST encapsulé](shutting-down-a-wrapped-pst-store-provider.md)
    
- Une fois que vous avez terminé d’utiliser un fournisseur de magasin PST encapsulé, vous devez arrêter correctement le fournisseur de magasin PST encapsulé.
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[D�veloppement d'un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

