---
title: MoveRecord, méthode (ADO)
TOCTitle: MoveRecord Method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd7496efe7c38fcd78800ad087730bb21a19c32e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470672"
---
# <a name="moverecord-method-ado"></a>MoveRecord, méthode (ADO)


**S’applique à**: Access 2013 | Office 2013
 

Déplace l'entité représentée par un objet [Record](record-object-ado.md) vers un autre emplacement.

## <a name="syntax"></a>Syntaxe

*Enregistrement*. MoveRecord (*Source*, *Destination*, *nom d’utilisateur*, *mot de passe*, *Options*, *asynchrone*)

## <a name="parameters"></a>Paramètres

  - *Source*

  - Facultatif. Valeur de type **String** qui contient une URL identifiant l'objet **Record** à déplacer. Si *Source* est omis ou spécifie une chaîne vide, l'objet représenté par cet **enregistrement** est déplacé. Par exemple si l'objet **Record** représente un fichier, le contenu du fichier est déplacé vers l'emplacement spécifié par le paramètre *Destination*.

  - *Destination*

  - Facultatif. Une valeur de **type String** qui contient une URL spécifiant l’emplacement où seront déplacées *Source* .

  - *Nom d’utilisateur*

  - Facultatif. Valeur de type **String** contenant l'ID utilisateur, qui le cas échéant, autorise l'accès à *Destination*.

  - *MotDePasse*

  - Facultatif. Valeur de type **String** contenant le mot de passe qui, le cas échéant, vérifie le paramètre *NomUtilisateur*.

  - *Options*

  - Facultatif. Valeur [MoveRecordOptionsEnum](moverecordoptionsenum.md) dont la valeur par défaut est **adMoveUnspecified**. Spécifie le comportement de cette méthode.

  - *Async*

  - Facultatif. Valeur de type **Boolean** qui, lorsqu'elle correspond à **True**, indique que cette opération doit être asynchrone.

## <a name="return-value"></a>Valeur de retour

Valeur de type **String**. En règle générale, la valeur de *Destination* est renvoyée. Toutefois, la valeur retournée précise dépend du fournisseur.

## <a name="remarks"></a>Notes

Les valeurs de la *Source* et de *Destination* ne doivent pas être identiques ; dans le cas contraire, une erreur d’exécution se produit. Il faut au moins que les noms de ressource, de chemin d'accès et de serveur diffèrent.

Pour les fichiers déplacés à l'aide du fournisseur de la publication Internet, cette méthode met à jour tous les liens hypertexte dans les fichiers déplacés sauf indication contraire précisée dans *Options*. Cette méthode échoue si *Destination* identifie un objet existant (fichier ou répertoire, par exemple), à moins que **adMoveOverWrite** soit spécifié.


> [!NOTE]
> <P>[!REMARQUE] Soyez prudent lorsque vous utilisez l'option <STRONG>adMoveOverWrite</STRONG>. Si, par exemple, vous spécifiez cette option lorsque vous déplacez un fichier vers un répertoire, le répertoire est supprimé et remplacé par le fichier.</P>



Certains attributs de l’objet **Record** , telles que la propriété [ParentURL](parenturl-property-ado.md) , ne seront pas mis à jour une fois cette opération terminée. Actualiser les propriétés de l’objet **Record** en fermant l' **enregistrement**, puis rouvrir avec l’URL de l’emplacement où le fichier ou répertoire a été déplacé.

Si l'objet **Record** a été obtenu d'un objet [Recordset](recordset-object-ado.md), le nouvel emplacement du fichier ou répertoire déplacé n'est pas directement reflété dans l'objet **Recordset**. Actualisez l'objet **Recordset** en le fermant puis en le rouvrant.


> [!NOTE]
> <P>[!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le <A href="microsoft-ole-db-provider-for-internet-publishing.md">fournisseur Microsoft OLE DB pour la publication Internet</A>. Pour plus d'informations, consultez <A href="absolute-and-relative-urls.md">URL absolues et relatives</A>.</P>


