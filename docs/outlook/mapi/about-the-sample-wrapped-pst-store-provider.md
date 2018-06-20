---
title: À propos de l’exemple de wrapper fournisseur de banque de dossiers personnels
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 953391ce-31a2-3271-365a-284cf5e15d82
description: 'Dernière modification : 03 juillet 2012'
ms.openlocfilehash: 51aef9d8778997749e401b008ebdb4126a248ee0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782851"
---
# <a name="about-the-sample-wrapped-pst-store-provider"></a>À propos de l’exemple de wrapper fournisseur de banque de dossiers personnels

 
  
**S’applique à**: Outlook 
  
## <a name="overview-of-message-store-providers"></a>Vue d’ensemble des fournisseurs de banque de messages

Fournisseurs de magasins message gérer le stockage et la récupération de messages et d’autres informations pour les utilisateurs d’applications clientes. Les informations du message sont organisées à l’aide d’un système hiérarchique appelé une banque de messages. La banque de messages est implémentée dans plusieurs niveaux, avec des conteneurs appelés dossiers qui contiennent des messages de types différents. Il n’existe aucune limite au nombre de niveaux dans une banque de messages ; les dossiers peuvent contenir le nombre de sous-dossiers.
  
Données de magasin de message peuvent être utilisées dans de diverses façons. Outre l’utilisation de messagerie par défaut, les dossiers peuvent être utilisés comme un forum de discussion publics, comme un référentiel de documents de référence ou en tant que conteneur pour les informations de forum. Une banque de messages unique peut contenir plusieurs types d’informations, certains modifiables et d’autres pas. Plusieurs clients peuvent installer la même base de messages, rendant simple et rapide de partager des données.
  
Dossiers de banque de messages vous permettent de trier et filtrer les messages et de personnaliser l’affichage en affichage de l’interface utilisateur. Liens vers les messages filtrés sont stockés dans des dossiers spéciaux appelés dossiers de résultats de recherche. L’utilisateur d’une application cliente entre les critères de filtrage qui MAPI fait référence à une restriction, et les critères est appliquée aux messages stockés dans un ou plusieurs dossiers. Par exemple, un utilisateur peut souhaiter afficher uniquement les messages affaire à un sujet particulier avec des dates d’arrivée qui sont le plus récent que la dernière semaine. Références pour les messages qui correspondent aux critères sont répertoriés dans le dossier de résultats de recherche et les messages réels restent dans leurs dossiers standard.
  
Les messages sont les unités de données transférées à partir d’un utilisateur ou une application à un autre utilisateur ou l’application. Chaque message contient certains le texte du message et les informations d’enveloppe de message qui sont utilisées pour la transmission. Certains messages contiennent une ou plusieurs pièces jointes, ou des données supplémentaires relatives aux transportés avec un message sous la forme d’un fichier, un autre message ou un objet OLE.
  
## <a name="the-sample-wrapped-pst-store-provider"></a>L’exemple de fournisseur de banque de dossiers personnels renvoyé à la ligne

L’API de réplication permet de répliquer des éléments d’un référentiel de données principale dans un magasin de PST d’Outlook. Vous utilisez l’API de réplication pour répliquer les données dans une banque de dossiers personnels dédiée et garder une trace de l’état de synchronisation. Cette approche ne nécessite pas d’introduire un fournisseur de banque MAPI personnalisé, qui est complexe pour écrire et mettre à jour. Toutefois, le fournisseur de banque PST a besoin d’être encapsulé pour fonctionner avec l’API de réplication.
  
Le fournisseur de banque PST encapsulé exemple utilise le fournisseur dossiers personnels (PST) en tant que serveur principal pour le stockage des données. Le fournisseur de banque PST encapsulé doit être utilisé conjointement avec l’API de réplication. Pour plus d’informations, consultez la rubrique [Sur l’API de réplication](about-the-replication-api.md). La plupart des fonctions dans le fournisseur de banque PST encapsulé exemple transmettre leurs arguments directement au fournisseur sous-jacent PST. Certaines fonctions requièrent une implémentation spéciale et sont décrites dans les rubriques suivantes.
  
## <a name="in-this-section"></a>Dans cette section

- [Installation de l’exemple de wrapper fournisseur de banque de dossiers personnels](installing-the-sample-wrapped-pst-store-provider.md)
    
- Explique comment télécharger et installer le fournisseur de banque exemple encapsulé PST.
    
- [L’initialisation d’un fournisseur de banque de dossiers personnels encapsulé](initializing-a-wrapped-pst-store-provider.md)
    
- La première étape dans l’implémentation d’un fournisseur de magasins PST encapsulé est à s’initialiser et configurer le fournisseur de banque PST justifié.
    
- [Se connecter à un fournisseur de banque de dossiers personnels encapsulé](logging-on-to-a-wrapped-pst-store-provider.md)
    
- Après l’initialisation d’un fournisseur de magasins PST encapsulé, vous devez implémenter les fonctions afin que MAPI et le spouleur MAPI peuvent se connecter au fournisseur de magasin PST justifié.
    
- [À l’aide d’un fournisseur de banque de dossiers personnels encapsulé](using-a-wrapped-pst-store-provider.md)
    
- Pour utiliser une banque de dossiers personnels encapsulée fournisseur, vous devez envelopper l’interface **[IMAPISupport::IUnknown](imapisupportiunknown.md)** pour implémenter courantes encapsulé tâches du fournisseur de magasin de fichiers PST. 
    
- [Arrêt d’un fournisseur de banque de dossiers personnels encapsulé](shutting-down-a-wrapped-pst-store-provider.md)
    
- Après avoir à l’aide d’un fournisseur de magasins PST encapsulé, vous devez fermer correctement le fournisseur de banque PST justifié.
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[D�veloppement d'un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

