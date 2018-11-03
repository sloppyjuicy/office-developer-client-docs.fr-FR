---
title: Informations détaillées sur HelloData (référence de base de données du bureau Access)
TOCTitle: HelloData details
ms:assetid: db51e15c-1b5b-c64a-2f84-34dd0e78c6cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250105(v=office.15)
ms:contentKeyID: 48548103
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ea7e89c47fc0886ed4240b7cb9a867fbfbfa93f7
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944773"
---
# <a name="hellodata-details"></a>Informations détaillées sur HelloData


**S’applique à**: Access 2013, Office 2013

L'application HelloData effectue les opérations de base d'une application ADO standard : extraction, vérification, modification et mise à jour des données. Lorsque vous démarrez l'application, cliquez sur le premier bouton, **Get Data**. Cette action déclenche l'exécution de la sous-routine GetData().

## <a name="getdata"></a>GetData

GetData place une chaîne de connexion valide dans une variable de niveau module *m\_sConnStr*. Pour plus d'informations sur les chaînes de connexion, consultez la rubrique [Création de la chaîne de connexion](creating-the-connection-string.md).

Affectez un gestionnaire d’erreurs utilisant une instruction Visual Basic **SurErreur**  Pour plus d’informations sur la gestion des erreurs dans ADO, consultez le [Chapitre 6 : Gestion des erreurs](chapter-6-error-handling.md). Un nouvel objet **Connection** est créé et la propriété **CursorLocation** a la valeur **adUseClient** car l’exemple HelloData crée un *jeu de données déconnecté*.  Cela signifie qu’une fois les données extraites de la source de données, la connexion physique à la source de données est interrompue mais que vous pouvez néanmoins continuer à travailler avec les données mises en cache localement dans votre objet **Recordset**

Après ouverture de la connexion, affectez une chaîne SQL à une variable (sSQL). Puis instanciez un nouvel objet **Recordset** , m\_oRecordset1. Dans la ligne suivante de code, ouvrez le **jeu d’enregistrements** existant **connexion**, en passant. Dans la ligne suivante de code, ouvrez le **jeu d’enregistrements** existant **connexion**, en passant sSQL comme source de l' **objet Recordset**. Vous aidez ADO à déterminer que la chaîne SQL transmise en tant que source du **Recordset** est une définition textuelle d'une commande en spécifiant **adCmdText** dans l'argument final de la méthode **Open** du **Recordset**. Cette ligne définit aussi les propriétés **LockType** et **CursorType** associées au **Recordset**.

La ligne de code suivante précise que la propriété **MarshalOptions** est égale à **adMarshalModifiedOnly**. **MarshalOptions** indique quels enregistrements doivent être marshalés vers le niveau intermédiaire (ou un serveur web). Pour plus d'informations sur le marshaling, voir la documentation COM. Lorsque vous utilisez **adMarshalModifiedOnly** avec un curseur côté client ([CursorLocation](cursorlocation-property-ado.md) = **adUseClient**), seuls les enregistrements qui ont été modifiés sur le client sont réécrits au niveau intermédiaire. Le fait de définir la propriété **MarshalOptions** sur **adMarshalModifiedOnly** peut améliorer les performances car les lignes à marshaler sont moins nombreuses.

Ensuite, déconnectez le **Recordset** en indiquant que sa propriété **ActiveConnection** est égale à **Nothing**. Pour plus d'informations, consultez la rubrique [Déconnexion et reconnexion de l'objet Recordset](disconnecting-and-reconnecting-the-recordset.md) dans le Chapitre 5 : Mise à jour et persistance des données.

Fermez la connexion à la source de données et détruisez l'objet **Connection** existant de façon à libérer les ressources qu'il utilise.

La dernière étape consiste à définir le **Recordset** comme **DataSource** de la grille Microsoft liée aux données sur le formulaire de façon à pouvoir afficher facilement les données du **Recordset** sur ce formulaire.

Cliquez sur le deuxième bouton, **Examine Data**. Cette action déclenche l'exécution de la sous-routine ExamineData.

## <a name="examinedata"></a>La sous-routine ExamineData

La sous-routine ExamineData utilise plusieurs méthodes et propriétés de l’objet **Recordset** pour afficher des informations sur les données dans le **jeu d’enregistrements**. Il indique le nombre d’enregistrements à l’aide de la propriété **RecordCount** . Il effectue une boucle dans le **Recordset** et imprime la valeur de la propriété **AbsolutePosition** dans la zone de texte sur le formulaire. Également dans la boucle, la valeur de la propriété **Bookmark** du troisième enregistrement est placée dans une variable variante *vBookmark*, pour une utilisation ultérieure.

La routine revient directement au troisième enregistrement grâce à la variable bookmark enregistrée précédemment. Elle appelle la sous-routine WalkFields qui exécute une boucle dans la collection **Fields** du **Recordset** et affiche les détails relatifs à chaque objet **Field** de la collection.

Enfin, ExamineData utilise la propriété **Filter** du **Recordset** pour filtrer les enregistrements selon le critère « CategoryId égale 2 ». L'application de ce filtre a un résultat immédiatement visible dans la grille d'affichage du formulaire.

Pour plus d'informations sur la fonctionnalité de la sous-routine ExamineData, consultez le [chapitre 3 : Examen des données](chapter-3-examining-data.md).

Cliquez ensuite sur le troisième bouton, **Edit Data**. Cette action déclenche l'exécution de la sous-routine EditData.

## <a name="editdata"></a>EditData

Lorsque le code entre la sous-routine EditData, le **Recordset** est toujours filtré sur CategoryId égale à 2, tel que seuls les éléments qui répondent aux critères de filtre sont visibles. Il parcourt tout d’abord le **jeu d’enregistrements** et augmente le prix de chaque élément visible dans le **jeu d’enregistrements** de 10 pour cent. La valeur du champ **prix** est modifiée en définissant la propriété **Value** de ce champ à un nouveau montant valid.

N'oubliez pas que le **Recordset** est déconnecté de la source de données. Les modifications apportées à EditData ne sont effectuées que sur la copie des données dans le cache local. Pour plus d'informations, consultez le [Chapitre 4 : Modification des données](chapter-4-editing-data.md).

Aucune modification ne sera apportée à la source de données tant que vous n'aurez pas cliqué sur le quatrième bouton, **Update Data**. Cette action déclenche l'exécution de la sous-routine UpdateData.

## <a name="updatedata"></a>UpdateData

La sous-routine UpdateData élimine d'abord le filtre appliqué au **Recordset**. Le code supprime et réinitialise comme **source de données** pour Microsoft liée aux données sur le formulaire afin que le **Recordset** non filtré s’affiche dans la grille.

Le code vérifie alors si vous pouvez revenir en arrière dans le **Recordset** en utilisant la méthode **Supports** avec l'argument **adMovePrevious**.

La routine passe au premier enregistrement grâce à la méthode **MoveFirst** et affiche les valeurs d'origine et actuelles du champ par le biais des propriétés **OriginalValue** et **Value** de l'objet **Field**. Ces propriétés, ainsi que la propriété **UnderlyingValue** (non utilisée ici), sont présentées au [Chapitre 5 : Mise à jour et persistance des données](chapter-5-updating-and-persisting-data.md).

Un nouvel objet **Connection** est ensuite créé et est utilisé pour rétablir la connexion à la source de données. Vous reconnectez le **Recordset** à la source de données en définissant le nouvel objet **Connexion** comme **ActiveConnection** du **Recordset**. Pour envoyer les mises à jour au serveur, le code appelle **UpdateBatch** sur le **Recordset**.

Si la mise à jour par lot réussit, une variable d’indicateur de module, est défini sur True. Cet indicateur vous rappellera ultérieurement de nettoyer toutes les modifications apportées à la base de données.

Enfin, le code revient au premier enregistrement du **Recordset** et affiche les valeurs d'origine et actuelles. Les valeurs sont identiques après l'appel de la méthode **UpdateBatch**.

Pour obtenir des informations plus détaillées sur la mise à jour des données, notamment ce qu'il faut faire lorsque les données du serveur sont modifiées alors que votre **Recordset** est déconnecté, consultez le [Chapitre 5 : Mise à jour et persistance des données](chapter-5-updating-and-persisting-data.md).

## <a name="formunload"></a>Formulaire\_Unload

Le formulaire\_sous-routine Unload est important pour plusieurs raisons. Tout d’abord, car il s’agit d’un exemple d’application, formulaire\_Unload nettoie les modifications apportées à la base de données avant la fermeture de l’application. Ensuite, le code montre comment une commande peut être exécutée directement à partir d'un objet **Connection** ouvert grâce à la méthode **Execute**. Enfin, il montre un exemple de l’exécution d’une requête ne retournant-ligne (une requête mise à jour) par rapport à la source de données.

