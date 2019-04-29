---
title: Déploiement de modèles de formulaire signés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8345a4bc-ad7b-d0b0-7615-f77ade35006d
description: Avant de lire cette rubrique, consultez la section « Modèles de formulaire signés » dans Autres concepts de sécurité pour les formulaires InfoPath pour une présentation de la sécurité des modèles de formulaire signés. Les informations et les explications de la rubrique Niveaux de sécurité, déploiement de courrier électronique et modèles de formulaire distants sont également pertinentes.
ms.openlocfilehash: 76cc6dfdbd2c01827182c348281a98ad7cd17b69
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426799"
---
# <a name="deploying-signed-infopath-form-templates"></a>Déploiement de modèles de formulaire signés

Avant de lire cette rubrique, consultez la section « Modèles de formulaire signés » dans [Autres concepts de sécurité pour les formulaires InfoPath](additional-infopath-form-security-concepts.md) pour une présentation de la sécurité des modèles de formulaire signés. Les informations et les explications de la rubrique [Niveaux de sécurité, déploiement de courrier électronique et modèles de formulaire distants](security-levels-email-deployment-and-remote-form-templates.md) sont également pertinentes. 
  
## <a name="digitally-signing-a-form-template"></a>Signature numérique d’un modèle de formulaire

Si vous signez numériquement un modèle de formulaire, vous pouvez définir le niveau de sécurité confiance totale pour le modèle de formulaire, ce qui signifie que le formulaire peut accéder aux fichiers et aux paramètres sur l'ordinateur de l'utilisateur ou sur un autre domaine. (En outre, la signature numérique d'un modèle de formulaire ne vous empêche pas d'utiliser d'autres niveaux de sécurité, si vous le souhaitez. Vous définissez le niveau de sécurité d'un modèle de formulaire signé sur le niveau de sécurité domaine ou restreint.) En outre, vous pouvez déployer le modèle de formulaire signé pour les utilisateurs qui utilisent un programme de messagerie électronique, puis mettre à jour ultérieurement automatiquement le modèle de formulaire signé en envoyant la version mise à jour aux utilisateurs sous la forme d'une pièce jointe à un message électronique, procédez comme suit:
  
### <a name="to-digitally-sign-a-form-template"></a>Pour signer numériquement un modèle de formulaire

1. Dans le Concepteur InfoPath, cliquez sur l'onglet **Fichier**, puis cliquez sur **Options de formulaire** sur l'onglet **Informations**. 
    
2. Dans la boîte de dialogue **Options de formulaire**, cliquez sur **Sécurité et approbation**. 
    
3. Sous **Signature du modèle de formulaire**, activez la case à cocher **Signer ce modèle de formulaire**. 
    
4. Cliquez sur **Sélectionner un certificat**.
    
5. Dans la boîte de dialogue **Sélectionner un certificat**, cliquez sur le certificat que vous voulez utiliser pour signer numériquement le modèle de formulaire. 
    
> [!NOTE]
> [!REMARQUE] Le bouton **Créer un certificat** de la boîte de dialogue **Options de formulaire** peut être utilisé pour générer un certificat de test pour signer un modèle de formulaire. Le certificat de test doit être utilisé pour signer des modèles de formulaire seulement à des fins de test. Les certificats de test ne doivent pas être utilisés pour signer des modèles de formulaire qui seront publiquement distribués. Les certificats n'étant pas émis par une Autorité de certification dont le certificat racine est déjà approuvé sur l'ordinateur d'un utilisateur, le certificat de test ne sera pas validé correctement sur l'ordinateur de l'utilisateur. Si vous déployez un modèle de formulaire signé avec un certificat de test, les utilisateurs de votre modèle de formulaire ne pourront probablement pas l'ouvrir. 
  
## <a name="establishing-a-trusted-root-certificate-and-publisher"></a>Établissement d’un certificat racine et d’un éditeur approuvés

 Le certificat racine approuvé du certificat qui est utilisé pour signer le modèle de formulaire doit se trouver dans le magasin de certificats racine approuvés de l'ordinateur client. Si ce n'est pas le cas, l'éditeur du modèle de formulaire ne peut pas être vérifié, et les utilisateurs de votre modèle de formulaire ne peut pas choisir d'approuver l'éditeur. Si le certificat racine approuvé se trouve dans le magasin de certificats racine approuvés mais que l'éditeur ne figure pas dans la liste des éditeurs approuvés, les utilisateurs peuvent choisir d'approuver l'éditeur du modèle de formulaire. 
  
> [!NOTE]
> [!REMARQUE] Si un modèle de formulaire signé demande un accès Domaine ou Restreint, InfoPath utilise la signature pour vérifier que le modèle de formulaire n'a pas été falsifié après avoir été signé. InfoPath utilise également la signature pour déterminer si le modèle de formulaire peut être mis à jour automatiquement. 
  
## <a name="deploying-signed-form-templates-with-full-trust-access"></a>Déploiement de modèles de formulaire signés avec un accès Confiance totale

Le scénario principal pour le déploiement de modèles de formulaire signés est d'activer une fonctionnalité similaire à celle d'un domaine, telle que la mise à jour automatique, dans des formulaires avec confiance totale. Un modèle de formulaire signé demandant un accès de type confiance totale a le même accès aux ressources système qu'un  *formulaire entièrement fiable*  . Pour une présentation détaillée de la façon dont fonctionnent les formulaires entièrement fiables et comment les déployer, voir [Présentation des formulaires entièrement fiables](understanding-fully-trusted-forms.md).
  
Cependant, en fonction de l'environnement informatique de votre organisation, vous pouvez préférer l'utilisation de modèles de formulaire signés ou celle de formulaires entièrement fiables. Par exemple, il y a des avantages à utiliser un modèle de formulaire signé qui demande un accès de type confiance totale au lieu d'un formulaire entièrement fiable et inscrit. Un modèle de formulaire signé demandant un accès de type confiance totale présente les avantages suivants :
  
- Il ne doit pas être inscrit, contrairement à un modèle de formulaire entièrement fiable non signé.
    
- Il permet la mise à jour automatique en mode silencieux du modèle de formulaire.
    
Dans la mesure où vous ne devez pas inscrire un modèle de formulaire signé qui demande un accès de type confiance totale, il n'est pas nécessaire d'utiliser un package d'installation ou un fichier de script pour le déployer. Cet avantage simplifie grandement le déploiement d'un modèle de formulaire avec confiance totale.
  
Lorsque vous mettez à jour votre modèle de formulaire signé qui demande un accès de type confiance totale, vous pouvez simplement envoyer le modèle mis à jour à l'utilisateur ou le mettre à jour à un emplacement partagé. Lorsque l'utilisateur ouvre le modèle mis à jour, aucun choix ne lui est proposé et la version mise à jour remplace silencieusement la copie plus ancienne sur l'ordinateur de l'utilisateur. Si vous avez mis à jour le modèle à un emplacement partagé, l'utilisateur peut utiliser la copie mise à jour sans qu'un choix lui soit proposé.
  
Si vous voulez mettre à jour un formulaire entièrement fiable non signé, vous devez replacer votre formulaire dans un package et le réinscrire. En outre, un modèle de formulaire entièrement fiable installé existant fonctionne seulement pour le chemin d'accès de l'ordinateur local, mais pas pour un chemin d'accès réseau, car le processus d'inscription ne prend pas en charge la modification d'un chemin d'accès d'ordinateur local en chemin d'accès réseau. Cependant, un certificat étant nécessaire pour signer un modèle de formulaire, il peut être préférable de déployer des modèles de formulaire entièrement fiables et inscrits si vous ne voulez pas acheter un certificat.
  
## <a name="deploying-signed-form-templates-with-domain-or-restricted-access"></a>Déploiement de modèles de formulaire signés avec un accès Domaine ou Restreint

Un modèle de formulaire signé qui a un niveau de sécurité Domaine ou Restreint bénéficie également de la fonctionnalité de mise à jour automatique. Par exemple, vous pouvez publier un modèle de formulaire signé dans une bibliothèque de documents sur un serveur exécutant Microsoft SharePoint Foundation ou sur un serveur qui a un niveau de sécurité Domaine. Lorsque vous mettez à jour votre modèle de formulaire à l'emplacement partagé, les utilisateurs reçoivent automatiquement la copie mise à jour.
  

