---
title: CopyRecord, méthode (ADO)
TOCTitle: CopyRecord Method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 73940108f96cf46cb15d646936039c0329373899
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606905"
---
# <a name="copyrecord-method-ado"></a>CopyRecord, méthode (ADO)


**S’applique à**: Access 2013 | Office 2013

Copie une entité représentée par un objet **Record** vers un autre emplacement.

## <a name="syntax"></a>Syntaxe

*Enregistrement*. CopyRecord (*Source*, *Destination*, *nom d’utilisateur*, *mot de passe*, *Options*, *asynchrone*)

## <a name="parameters"></a>Paramètres

  - *Source*

  - Facultatif. Valeur de type **String** contenant une URL spécifiant l'entité à copier (par exemple, un fichier ou un répertoire). Si la *Source* est omis ou spécifie une chaîne vide, le fichier ou le répertoire représenté par l' [enregistrement](record-object-ado.md) actif est copié.

  - *Destination*

  - Facultatif. Une valeur de **type String** qui contient une URL spécifiant l’emplacement dans lequel *Source* va être copié.

  - *Nom d’utilisateur*

  - Facultatif. Valeur de type **String** contenant l'ID utilisateur, qui le cas échéant, autorise l'accès à *Destination*.

  - *MotDePasse*

  - Facultatif. Valeur de type **String** contenant le mot de passe qui, le cas échéant, vérifie le paramètre *NomUtilisateur*.

  - *Options*

  - Facultatif. Valeur de l'énumération [CopyRecordOptionsEnum](copyrecordoptionsenum.md) (par défaut, **adCopyUnspecified** ). Spécifie le comportement de cette méthode.

  - *Async*

  - Facultatif. Valeur de type **Boolean** qui, lorsqu'elle correspond à **True**, indique que cette opération doit être asynchrone.

<<<<<<< Tête
## <a name="return-value"></a>Valeur renvoyée
=======
## <a name="return-value"></a>Valeur renvoyée
>>>>>>> master

Valeur de type **String** qui retourne, en général, la valeur de *Destination*. Toutefois, la valeur exacte renvoyée dépend du fournisseur.

## <a name="remarks"></a>Remarques

Les valeurs de la *Source* et de *Destination* ne doivent pas être identiques ; dans le cas contraire, une erreur d’exécution se produit. Il faut au moins que le nom du serveur, du chemin d'accès ou de la ressource diffère.

Tous les enfants (par exemple, les sous-répertoires) de *Source* sont copiés de manière récursive sauf si la valeur **adCopyNonRecursive** est spécifiée. Dans une opération récursive, *Destination* ne doit pas correspondre à un sous-répertoire de *Source* sans quoi l'opération n'est pas exécutée.

Cette méthode échoue si *Destination* identifie une entité existante (par exemple, un fichier ou un répertoire) sauf si **adCopyOverWrite** est spécifié.


> [!IMPORTANT]
> <P>[!IMPORTANTE] Soyez prudent lorsque vous utilisez l'option <STRONG>adCopyOverWrite</STRONG>. Par exemple, si cette option lors de la copie d’un fichier dans un répertoire sera <EM>Supprimer</EM> le répertoire et remplacez-la par le fichier.</P>




> [!NOTE]
<<<<<<< Tête
> <P>[!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le <A href="microsoft-ole-db-provider-for-internet-publishing.md">fournisseur Microsoft OLE DB pour la publication Internet</A>. Pour plus d'informations, consultez <A href="absolute-and-relative-urls.md">URL absolues et relatives</A>.</P>
=======
> [!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md). Pour plus d’informations, consultez [URL absolues et relatives](absolute-and-relative-urls.md).
>>>>>>> master


