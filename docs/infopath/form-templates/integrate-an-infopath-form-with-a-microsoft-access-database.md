---
title: Intégration d'un formulaire InfoPath à une base de données Microsoft Access
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 5ec9a9c0-b348-4a31-b377-e95db2f92455
description: Microsoft InfoPath permet l'utilisation d'une base de données Microsoft Access 2010 comme source de données principale pour un formulaire, ou comme source de données secondaire pour un formulaire ou un contrôle. Cet article explique comment utiliser une base de données Access 2010 comme source de données.
ms.openlocfilehash: 3cdc5b775ab7890604b33afa707bce6c55034e25
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584793"
---
# <a name="integrate-an-infopath-form-with-a-microsoft-access-database"></a>Intégration d'un formulaire InfoPath à une base de données Microsoft Access

Microsoft InfoPath permet l'utilisation d'une base de données Microsoft Access 2010 comme source de données principale pour un formulaire, ou comme source de données secondaire pour un formulaire ou un contrôle. Cet article explique comment utiliser une base de données Access 2010 comme source de données.
  
## <a name="using-a-microsoft-access-database-as-a-data-source"></a>Utilisation d'une base de données Microsoft Access en tant que source de données

### <a name="setting-up-a-microsoft-access-database-as-a-forms-primary-data-source"></a>Configuration d'une base de données Microsoft Access en tant que source de données principale de formulaire

Les connexions de base de données sont établies dans InfoPath à l'aide de l' **Assistant Connexion de données**. Pour ouvrir cet assistant, sélectionnez **Base de données** dans la section **Modèles de formulaires avancés** de l'onglet **Nouveau** de Microsoft Office Backstage, puis cliquez sur **Modifier ce formulaire**.
  
Cliquer sur **Sélectionner la base de données** vous permet de choisir une source de données existante ou de vous connecter directement à un fichier de base de données spécifique.
  
Lorsque vous avez sélectionné une base de données, l'assistant vous invite à sélectionner une table dans la base de données à utiliser comme source de données pour le formulaire. À mesure que vous ajoutez des tables, les relations qui les lient s'établissent et l'assistant affiche les tables et leurs relations hiérarchiques dans la liste **Structure de la source de données**. Si vous activez la case à cocher **Afficher les colonnes de la table**, l'assistant affiche les noms des champs de chaque table dans la liste Structure de la source de données ; utilisez les cases à cocher en regard de chaque nom de champ pour spécifier son inclusion dans l'instruction SQL que l'assistant construit. 
  
> [!NOTE]
> [!REMARQUE] Les champs de clé primaires sont toujours sélectionnés et ne peuvent pas être supprimés. 
  
Lorsque les tables, les relations et les champs ont été spécifiés à l'aide de l' **Assistant Connexion de données**, vous pouvez cliquer sur **Modifier SQL** pour afficher l'instruction SQL qui sera utilisée pour établir la source de données pour le formulaire. Dans la boîte de dialogue **Modifier SQL**, vous pouvez cliquer sur **Tester l'instruction SQL** pour vérifier que InfoPath sera en mesure de créer la source de données à partir des informations fournies. Vous pouvez également utiliser la boîte de dialogue **Modifier SQL** pour modifier l'instruction SQL de sorte de créer des requêtes complexes. 
  
> [!NOTE]
> [!REMARQUE] Les instructions SQL utilisées par InfoPath sont des requêtes de mise en forme des données. Les requêtes de mise en forme des données permettent de construire des relations hiérarchiques entre deux entités logiques ou plus au sein d'une requête. Il est possible d'utiliser des instructions SQL JOIN mais cela n'est pas recommandé car cette méthode désactive l'envoi du formulaire. Pour plus d'informations sur les requêtes de mise en forme des données, consultez la documentation MSDN (Microsoft Developer Network). 
  
La dernière page de l' **Assistant Connexion de données** affiche un résumé sur la source de données, indiquant notamment le nom et l'emplacement du fichier de la source de données, le nom de la table parent primaire, le nombre de tables utilisées et l'état d'envoi. L'état d'envoi vous indique si l'instruction SQL générée permettra d'envoyer les données à la source. 
  
### <a name="setting-up-a-microsoft-access-database-as-a-secondary-data-source"></a>Configuration d'une base de données Microsoft Access en tant que source de données secondaire

Les sources de données secondaires peuvent par exemple fournir les entrées d'une zone de liste ou d'une liste déroulante, mais vous pouvez aussi écrire du code afin d'insérer des données en provenance d'une source de données secondaire dans votre formulaire. Pour utiliser des sources de données secondaires avec votre formulaire, cliquez sur **Connexions de données** dans l'onglet **Données** lors de la conception d'un formulaire. 
  
Au démarrage de l' **Assistant Connexion de données**, vous êtes invité à spécifier la réception de données à utiliser dans vote formulaire, ou l'envoi de données dans le formulaire. Choisissez **Réception des données**, puis cliquez sur **Suivant**. Pour créer une source de données secondaire à partir d'une base de données, activez **Base de données (Microsoft SQL Server ou Microsoft Office Access uniquement)**. Dans la page suivante de l'assistant, cliquez sur **Sélectionner une base de données** pour choisir une source de données existantes ou vous connecter directement à un fichier de base de données spécifique. 
  
Lorsque vous avez sélectionné une base de données, l'assistant vous invite à sélectionner une table ou une requête dans la base de données à utiliser comme source de données pour le formulaire. Vous devez sélectionner une table ou une requête pour commencer, mais vous pouvez en sélectionner d'autres ultérieurement si vous souhaitez les inclure. Lorsque vous avez sélectionné une table ou une requête, l'assistant vous permet de sélectionner les champs à utiliser dans la liste **Structure de la source de données**. Par défaut, tous les champs de la table sont sélectionnés, mais vous pouvez supprimer ceux qui ne sont pas nécessaires à votre formulaire. Vous pouvez également déterminer la manière avec laquelle les enregistrements renvoyés de la table sont triés, et si les enregistrements multiples sont autorisés. Pour ce faire, cliquez sur **Modifier la table**, puis sélectionnez jusqu'à trois critères de tri dans la boîte de dialogue **Ordre de tri**. Lorsque vous êtes satisfait, cliquez sur **Terminer**.
  
> [!NOTE]
> [!REMARQUE] Les champs de clé primaires sont toujours sélectionnés et ne peuvent pas être supprimés. 
  
InfoPath vous permet également de récupérer des données dans plusieurs tables ou requêtes à la fois. Lorsque vous récupérez des données provenant de tables ou requêtes multiples, vous devez pouvoir établir une relation entre toutes les tables ou les requêtes associées à la table ou à la requête d'origine que vous avez sélectionnée dans l' **Assistant Connexion de données**. Par exemple, si vous récupérez des données depuis la table Clients de la base de données Northwind, vous pouvez ajouter la table Commandes pour y récupérer des données sur toutes les commandes associées à tel client, et ajouter la table Détails commandes pour y récupérer les détails de chaque commande.
  
Pour ajouter une table supplémentaire à la source de données, sélectionnez la table à laquelle vous voulez ajouter une table enfant dans la liste **Structure de la source de données**, puis cliquez sur **Ajouter une table**. Sélectionnez la table ou la requête que vous souhaitez ajouter, puis cliquez sur **Suivant**. InfoPath vous invite à sélectionner la ou les relations à utiliser. Si des champs des deux tables portent le même nom, InfoPath ajoute automatiquement ces champs en tant que relation, mais si tel n'est pas le cas, ou si vous préférez utiliser une relation personnalisée, vous pouvez cliquer sur **Ajouter une relation** pour spécifier quels champs correspondent aux champs de la table enfant. Vous pouvez également supprimer des relations existantes en cliquant sur **Supprimer la relation** dans la boîte de dialogue **Modifier la relation**. 
  
Lorsque vous êtes satisfait des relations définies, cliquez sur **Terminer**. À l'instar de la table principale, vous pouvez spécifier quels champs sont renvoyés depuis la table enfant. Toutefois, vous ne pouvez pas utiliser le bouton **Modifier la table** pour changer l'ordre dans lequel sont renvoyés les enregistrements. 
  
Lorsque les tables, les relations et les champs ont été spécifiés, vous pouvez cliquer sur **Modifier SQL** pour afficher l'instruction de requête SQL qui sera utilisée pour établir la source de données pour le formulaire. Dans la boîte de dialogue **Modifier SQL**, vous pouvez cliquer **Tester l'instruction SQL** pour vérifier que InfoPath sera en mesure de créer la source de données à partir des informations fournies. Vous pouvez également utiliser la boîte de dialogue **Modifier SQL** pour modifier l'instruction SQL de sorte de créer des requêtes complexes. 
  
> [!NOTE]
> [!REMARQUE] Les instructions SQL utilisées par InfoPath sont des requêtes de mise en forme des données. Les requêtes de mise en forme des données permettent de construire des relations hiérarchiques entre deux entités logiques ou plus au sein d'une requête. Il est possible d'utiliser des instructions SQL JOIN mais cela n'est pas recommandé, car cette méthode désactive l'envoi du formulaire. Pour plus d'informations sur les requêtes de mise en forme des données, consultez la documentation MSDN (Microsoft Developer Network). 
  
## <a name="enabling-form-submission"></a>Activation de l'envoi de formulaire

En plus de recevoir des données en provenance d'une base de données Access, InfoPath peut envoyer des données nouvelles ou en renvoyer des modifiées à la base de données. Lorsque vous utilisez la commande **Envoyer** dans l'onglet **Accueil** ou le Microsoft Office Backstage pour envoyer les modifications à la base de données, InfoPath utilise ActiveX Data Objects (ADO) pour mettre à jour les enregistrements dans la base de données. L'envoi de formulaire est activé lorsque toutes les conditions suivantes sont remplies : 
  
- Il doit y avoir une colonne de base pour chaque colonne utilisée dans la requête du formulaire.
    
- Une colonne de table ne peut pas apparaître plusieurs fois dans la requête.
    
- Une clé primaire, une contrainte unique ou un index unique doit être disponible pour chaque table d'une clause SELECT qui est utilisée dans la requête du formulaire.
    
- Une table ne peut pas être incluse plusieurs fois dans la requête du formulaire.
    
- Les relations entre tables parent et enfant doivent inclure toutes les colonnes de clé primaires présentes dans la table parent.
    
- Il ne peut y avoir qu'une seule table de base pour toutes les colonnes d'une clause SELECT qui est utilisée dans la requête du formulaire.
    
Certaines circonstances empêchent InfoPath d'envoyer les modifications apportées aux formulaires à une base de données. Par exemple, si vous créez un formulaire qui trace les données depuis une requête plutôt qu'une table, ou si vous personnalisez l'instruction SQL qui est utilisée par InfoPath de sorte d'inclure une instruction JOIN, InfoPath sera incapable d'envoyer les modifications. Autre circonstance susceptible d'empêcher InfoPath d'envoyer les modifications : vous ajoutez dans le formulaire des tables ayant des relations plusieurs-à-un avec leur table parent. Dans les situations où InfoPath est incapable d'envoyer les modifications à la base de données, le champ **État de l'envoi**, à la dernière page de l' **Assistant Connexion de données** affichera la raison de cette empêchement. 
  

