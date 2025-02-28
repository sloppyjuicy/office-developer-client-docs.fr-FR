---
title: Utiliser SharePoint membres du modèle objet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 8cbafca3-7831-4231-8e61-38330b5ad61b
description: avant de pouvoir programmer en faisant référence aux membres du modèle objet de SharePoint à partir du code exécuté dans un modèle de formulaire InfoPath, vous devez référencer l'assembly Microsoft.SharePoint.dll dans le projet Visual Studio 2012 de votre formulaire. Pour cela, vous devez avoir accès au système de fichiers d'une copie de Microsoft SharePoint Server 2010 ou à un serveur Microsoft SharePoint Foundation 2010 afin de pouvoir obtenir une copie de l'assembly Microsoft.SharePoint.dll.
ms.openlocfilehash: c23997c62593bf5a9736d1593afd39b11c96422f
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381326"
---
# <a name="use-sharepoint-object-model-members"></a>Utiliser SharePoint membres du modèle objet

avant de pouvoir programmer en faisant référence aux membres du modèle objet de SharePoint à partir du code exécuté dans un modèle de formulaire InfoPath, vous devez référencer l'assembly Microsoft.SharePoint.dll dans le projet Visual Studio 2012 de votre formulaire. Pour cela, vous devez avoir accès au système de fichiers d'une copie de Microsoft SharePoint Server 2010 ou à un serveur Microsoft SharePoint Foundation 2010 afin de pouvoir obtenir une copie de l'assembly Microsoft.SharePoint.dll.
  
En outre, votre modèle de formulaire doit être déployé sur le serveur en tant que solution sandbox ou solution approuvée par l'administrateur. Pour plus d'informations sur ces options de déploiement, voir [Publication de formulaires avec code](publishing-forms-with-code.md).
  
## <a name="add-and-reference-the-microsoftsharepoint-assembly-from-an-infopath-form-template"></a>Ajouter l’assembly Microsoft.SharePoint et le référencer depuis un modèle de formulaire InfoPath

> [!IMPORTANT]
> [!IMPORTANTE] Pour éviter un conflit avec la manière dont le projet InfoPath gère les fichiers ajoutés au fichier de modèle du formulaire, ne copiez aucun des assemblys que vous souhaitez référencer dans le dossier du niveau le plus élevé du projet de modèle de formulaire. Par défaut, il s’agit d’un chemin d’accès au format suivant : < *drive* >:\Users\ *UserName*  \Documents\InfoPath Projects\ *ProjectName* > Si vous souhaitez déplacer des assemblys que vous référencez à un emplacement dans le dossier du projet, vous devez créer un sous-dossier sous le dossier de projet *ProjectName*  principal, puis copier et référencer des assemblys à partir de ce sous-dossier. Cependant, la création d'un sous-dossier pour les assemblys référencés n'est pas nécessaire. Tant qu'un assembly référencé ne se trouve pas dans le dossier de niveau supérieur du projet, le projet InfoPath copie l'assembly dans le fichier de modèle de formulaire (.xsn) lorsque le projet est compilé et publié.
  
Par défaut, Microsoft.SharePoint.Server.dll est installé dans C:\Program Files\Common Files\Microsoft Shared\Web Server\Extensions\14\ISAPI dans le système de fichiers SharePoint Server 2010 ou sur un serveur SharePoint Foundation 2010.
  
### <a name="to-reference-the-microsoftsharepoint-assembly-from-an-infopath-forms-code-project"></a>Pour faire référence à l’assembly Microsoft.SharePoint depuis le projet de code d’un formulaire InfoPath

1. Copiez l'assembly Microsoft.SharePoint.Server.dll depuis le serveur vers un dossier local ou accédez-y depuis un dossier partagé.

2. Ouvrez le projet de modèle de formulaire dans Visual Studio 2012.

3. Dans le menu **Projet**, cliquez sur **Ajouter une référence**.

4. Cliquez sur l'onglet **Parcourir**, recherchez l'assembly, puis cliquez sur **OK** pour ajouter la référence.

Vous pouvez maintenant écrire du code faisant référence aux membres du modèle objet de SharePoint à partir du code de votre formulaire. Pour faciliter le référencement des membres de Microsoft. SharePoint’espace de noms, ajoutez `using Microsoft.SharePoint;` `Imports Microsoft.SharePoint` ou ajoutez-le aux directives au début de votre fichier de code. Pour consulter un exemple de l'utilisation des membres du modèle objet de SharePoint dans un formulaire InfoPath, voir « Exemple 2 : gestion des fournisseurs dans une liste SharePoint » dans [Exemples de solutions en bac à sable (sandbox)](sample-sandboxed-solutions.md).
