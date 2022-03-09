---
title: Niveaux de sécurité, déploiement de messagerie et modèles de formulaire distants
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7fc438ad-ae26-3632-3444-371537eaecb3
description: Microsoft InfoPath prend en charge le déplacement de modèles de formulaires d’un emplacement à un autre, leur envoi sous forme de pièce jointe à un message électronique et la création de modèles de formulaires De confiance totale signés ou installés numériquement.
ms.openlocfilehash: 0f20a1f6cc8197b19d8dfcc95eb6da97fc1140b3
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380563"
---
# <a name="security-levels-email-deployment-and-remote-form-templates"></a>Niveaux de sécurité, déploiement de messagerie et modèles de formulaire distants

Microsoft InfoPath prend en charge le déplacement de modèles de formulaires d’un emplacement à un autre, leur envoi sous forme de pièce jointe à un message électronique et la création de modèles de formulaires De confiance totale signés ou installés numériquement.
  
## <a name="security-levels"></a>Niveaux de sécurité

Les modèles peuvent avoir trois niveaux de sécurité, suivant leur emplacement. Ces trois niveaux de sécurité sont définis dans les sections suivantes.
  
### <a name="restricted"></a>Restreint

Le niveau de sécurité Restreint n'autorise aucune communication en dehors du modèle de formulaire. Ce niveau de sécurité permet d'éviter que les formulaires dangereux transmettent des données de votre ordinateur à un utilisateur malintentionné. Dans ce mode de sécurité, les fonctionnalités suivantes sont inopérantes :
  
- Volets de tâches HTML  
- Requête SharePoint
- Envoi SharePoint
- Requête de fichier XML
- Requête de base de données
- Envoi de base de données
- Requête de service Web
- Envoi de service Web
- Envoi de code personnalisé
- Envoi d'environnement d'hébergement
- Contrôles ActiveX
- Rôles
- Flux de travail SharePoint
- Règles qui ouvrent un nouveau document
- Code managé
- Mode Page externe
- Images liées

### <a name="domain"></a>Domain

Le niveau de sécurité Domaine limite un formulaire à un domaine Internet particulier et restreint ses autorisations aux paramètres Internet Explorer de la zone dans laquelle se trouve le domaine. Le formulaire est autorisé à communiquer avec d'autres sources de données à l'intérieur de son propre domaine mais n'est généralement pas autorisé à récupérer des données provenant d'autres domaines à moins que la zone autorise la communication inter-domaine. Il s'agit du niveau de sécurité minimum autorisé pour les modèles de formulaire compatibles avec les navigateurs.
  
### <a name="full-trust"></a>Confiance totale

Le niveau de sécurité Confiance totale vous permet d'exécuter un formulaire en confiance totale sur l'ordinateur où il va être utilisé. Ce niveau de sécurité ne peut s'utiliser que lorsque vous travaillez avec un formulaire situé sur un serveur et signé d'une signature correspondant à un éditeur racine de confiance sur votre ordinateur, ou lors de l'installation du formulaire. Les deux méthodes nécessitent de paramétrer l'attribut **requireFullTrust** en « yes ». Avec ce paramètre, le formulaire peut accéder à des appels de modèle d'objet tels que l'enregistrement de fichier, et certaines invites de sécurité apparaissant dans les niveaux de sécurité plus restrictifs sont désactivées.
  
> [!NOTE]
> [!REMARQUE] Tous les formulaires générés dans le concepteur InfoPath sont associés à un niveau de sécurité. InfoPath ouvre les formulaires à leur niveau de sécurité associé. Si le niveau de sécurité associé au formulaire est plus élevé que le niveau de sécurité pouvant lui être accordé, le formulaire ne s'ouvrira pas.
  
Le niveau de sécurité Confiance totale ne peut être défini que pour les modèles de formulaire installés ou signés ; autrement le niveau de confiance maximum est Domaine. InfoPath ne définit pas automatiquement le niveau de sécurité Confiance totale.
  
Les formulaires reçoivent leur niveau de sécurité en fonction de l'emplacement à partir duquel le formulaire est ouvert.
  
## <a name="trust-levels"></a>Niveaux de confiance

Le niveau de confiance le plus élevé pouvant être accordé à un modèle de formulaire est déterminé par l'emplacement Ouvert à partir de et par un code de vérification, comme indiqué dans la table suivante. Les attributs répertoriés dans le tableau (par exemple, HTTP, UNC, *requireFullTrust*) sont des entrées utilisées pour déterminer le niveau de confiance qui peut être accordé à un formulaire et qui s’appliquent aux formulaires ouverts dans le client InfoPath.
  
|Niveau de confiance accordé le plus élevé|Confiance totale|Ordinateur client (mode bac à sable)|Intranet (mode bac à sable)|Internet (mode bac à sable)|Restreint|
|:-----|:-----:|:-----:|:-----:|:-----:|:-----:|
|**fichier : chemin d'accès=emplacement d'ouverture** <br/> |||X  <br/> |||
|**file: Access PathOpened\<\> From Location or no Access Path (regardless of where the form came from)** <br/> |||||X  <br/> |
|**Emplacement d'ouverture : Intranet HTTP ou HTTPS** <br/> |||X  <br/> |||
|**Emplacement d'ouverture : Internet HTTP ou HTTPS** <br/> ||||X  <br/> ||
|**Emplacement d'ouverture : UNC** <br/> |||X  <br/> |||
|**Modèle installé (requireFullTrust="yes")** <br/> |X  <br/> |||||
|**Modèle installé (requireFullTrust="no")** <br/> ||X  <br/> ||||
|**Modèle avec certificat d'éditeur approuvé** <br/> |X  <br/> |||||
|**Fichiers de formulaire exportés** <br/> |||X  <br/> |||

## <a name="form-open-behavior"></a>Comportement d’ouverture des formulaires

Tous les fichiers de formulaire ouverts dans l'éditeur InfoPath sont liés par un ensemble de conditions qui déterminent le niveau de sécurité auquel le formulaire s'ouvre, s'il s'ouvre. Lorsqu'un formulaire InfoPath est ouvert dans l'éditeur, il s'ouvre au niveau de sécurité approprié, ou ne s'ouvre pas du tout. Si un formulaire demande un niveau de sécurité supérieur à celui pouvant lui être accordé (un formulaire peut demander un niveau de sécurité spécifique à l'aide de l'attribut **trustLevel** ou **requireFullTrust**), il n'est pas autorisé à se charger. Si le niveau de sécurité demandé peut lui être accordé, il est chargé au niveau demandé. Si le modèle de formulaire n'est pas autorisé à s'ouvrir au niveau de sécurité demandé, l'utilisateur ne peut pas ouvrir le formulaire et reçoit un message d'erreur.
  
La table suivante décrit les conditions requises pour l'ouverture d'un formulaire à chaque niveau de sécurité, ainsi que le comportement qui se produit lorsque l'utilisateur essaie d'ouvrir le formulaire.
  
|L'éditeur ouvre/échoue|Confiance totale (requireFullTrust="yes")|Confiance Domaine (trustLevel="Domain" ou vide)|Restreint (trustLevel="Restricted")|
|:-----|:-----|:-----|:-----|
|**Approuvé (installé ou certificat d'approbation)** <br/> |L'éditeur ouvre au niveau Confiance totale  <br/> |N/A  <br/> |N/A  <br/> |
|**Confiance de domaine : Ordinateur client** <br/> |Échec d'ouverture  <br/> |L’éditeur s’ouvre au niveau du domaine  <br/> |L'éditeur ouvre au niveau Restreint  <br/> |
|**Confiance Domaine : Intranet** <br/> |Échec d'ouverture  <br/> |L’éditeur s’ouvre au niveau du domaine  <br/> |L'éditeur ouvre au niveau restreint  <br/> |
|**Confiance Domaine : Internet** <br/> |Échec d'ouverture  <br/> |L’éditeur s’ouvre au niveau du domaine  <br/> |L'éditeur ouvre au niveau restreint  <br/> |
|**Restricted** <br/> |Échec d'ouverture  <br/> |Échec d'ouverture  <br/> |L'éditeur ouvre au niveau restreint  <br/> |

## <a name="specifying-a-security-level"></a>Spécification d’un niveau de sécurité

Le concepteur de formulaires InfoPath sélectionne automatiquement le niveau de sécurité approprié (Restreint ou Domaine) d'après les fonctionnalités que vous utilisez dans le formulaire. Le paramètre de sécurité est toujours aussi restrictif que possible, en commençant au niveau Restreint, pour vous garantir un niveau de protection optimale, pour vous et vos données. Les utilisateurs peuvent modifier manuellement ce paramètre automatique et sélectionner un niveau de sécurité plus approprié pour le formulaire en suivant ces étapes :
  
1. Cliquez sur l'onglet **Fichier**, puis cliquez sur **Options de formulaire** sous l'onglet **Infos**.

2. Dans la liste **Catégories**, cliquez sur **Sécurité et approbation**.

3. Désactivez la case à cocher **Déterminer automatiquement le niveau de sécurité (recommandé)**.

4. Sélectionnez le niveau de sécurité souhaité.

## <a name="mail-deployment-and-browser-enabled-form-templates"></a>Déploiement de messagerie et modèles de formulaires activés pour le navigateur

InfoPath vous permet d’envoyer vos modèles de formulaire en pièce jointe à un message électronique et de les déplacer d’un emplacement à un autre. Le déploiement par courrier est un moyen simple et efficace pour distribuer des formulaires destinés à un usage au bureau ou pour déployer des formulaires à destination d'utilisateurs distants.
  
Par ailleurs, si vous disposez de Microsoft SharePoint Server 2010 avec InfoPath Forms Services, vous pouvez créer des modèles de formulaire qui permettent aux utilisateurs ne possédant pas InfoPath de remplir des formulaires dans un navigateur Web.
  
## <a name="understanding-form-identity"></a>Comprendre l’identité du formulaire

Tous les formulaires du concepteur InfoPath sont créés avec une identité. Ces informations d'identité aident InfoPath à associer les formulaires aux modèles de formulaire dans le cache et à récupérer les mises à jour des formulaires lorsqu'elles sont publiées sur un emplacement partagé. Par défaut, InfoPath crée deux identités pour les modèles de formulaire : un ID de formulaire et un chemin d'accès.
  
### <a name="form-id"></a>ID de formulaire

L'ID de formulaire est un identificateur unique composé d'un préfixe, du nom du formulaire et de l'espace de noms du formulaire. L'identificateur doit être un nom unique pouvant être utilisé pour associer correctement des fichiers de formulaire avec le modèle de formulaire voulu dans le cache de l'ordinateur client. L’ID de formulaire est spécifié en tant qu’attribut de nom (par exemple) `name="urn:MyForm:MyCompany:Template1:myXSD-1583-78-G3V94-23-47"`dans le fichier de définition du formulaire (.xsf).
  
### <a name="access-path"></a>Chemin d'accès

Le chemin d'accès est un identificateur d'emplacement utilisé pour déterminer l'emplacement correct du modèle de formulaire ainsi que l'emplacement de réception des mises à jour. Une fois le modèle de formulaire enregistré ou publié, l'emplacement où le modèle de formulaire est enregistré ou publié devient le chemin d'accès par défaut. Chaque fois qu'un formulaire est ouvert sur l'ordinateur client, le formulaire essaie de s'associer à un formulaire en cache. Il essaiera de le faire dans l'ordre suivant :
  
1. Rechercher un modèle de formulaire entièrement approuvé doté d'un ID de formulaire correspondant.

2. Rechercher un modèle de formulaire doté d'un chemin d'accès correspondant dans le cache.

3. Rechercher un modèle de formulaire doté d'un ID de formulaire correspondant dans le cache.

Une fois la correspondance établie, le formulaire s'ouvre avec le modèle de formulaire associé. Dans les cas où la correspondance a été établie avec un chemin d'accès, InfoPath utilisera le chemin d'accès pour récupérer les mises à jour du modèle de formulaire. Cette méthode simplifie l'administration d'entreprise, la maintenance et la mise à jour des formulaires. Dans les cas où la correspondance ne peut pas être établie et que le niveau de confiance est Domaine, le formulaire ne s'ouvre pas. Le chemin d'accès est spécifié en tant qu'attribut **publishUrl** dans le fichier de définition de formulaire (.xsf).
  
Tout comme chaque modèle de formulaire possède deux propriétés d'identification, il existe un jeu de paramètres heuristiques permettant de déterminer spécifiquement les entrées résultantes dans le cache, d'après la condition du modèle de formulaire (s'il possède un chemin d'accès, un ID de formulaire ou les deux) et l'état de la connexion réseau.
  
## <a name="designing-a-form-to-send-as-an-attachment-to-an-email-message"></a>Conception d’un formulaire à envoyer en tant que pièce jointe à un message électronique

Tous les formulaires créés dans le concepteur InfoPath peuvent être envoyés aux utilisateurs en tant que pièces jointes à un message électronique. Le déploiement de courrier électronique est un moyen simple et efficace de distribuer des formulaires à des usages inter-offices et de déployer des formulaires pour des utilisateurs distants.
  
### <a name="to-mail-a-form-template-to-other-users"></a>Pour envoyer un modèle de formulaire à d'autres utilisateurs par courrier électronique

1. Cliquez sur **l’onglet** Fichier, sur **Publier**, puis sur le bouton **Courrier** électronique.

2. Renseignez les deux pages suivantes de l' **Assistant Publication** en cliquant sur **Suivant** pour accéder à la page suivante, puis cliquez sur **Publier**.

3. Un message électronique s’affiche, ce qui vous permet de remplir la liste des destinataires et les instructions supplémentaires que vous pouvez leur donner.

4. Une fois terminé, cliquez sur **Envoyer**. Le formulaire et le modèle seront joints au message.

## <a name="email-deployment-restricted-domain-and-full-trust-form-templates"></a>Déploiement de messagerie électronique : modèles de formulaires restreints, de domaine et de confiance totale

Le déploiement par courrier électronique de modèles de formulaires restreints permet d’ouvrir des formulaires dynamiques sans connexion de données depuis n’importe où. Les destinataires peuvent ouvrir des modèles de formulaire envoyés sous forme de pièces jointes de courrier électronique directement depuis Microsoft Outlook 2010 ou depuis l’endroit où le destinataire a enregistré la pièce jointe. De plus, Outlook 2010 permet aux utilisateurs de modifier les formulaires directement dans le message.
  
Les modèles de formulaire avec le niveau de confiance Domaine doivent être ouverts à partir de leur emplacement publié, mais en publiant dans une liste de destinataires de courrier dans l’Assistant Publication, ils peuvent être envoyés en tant que pièces jointes à un message électronique. Lorsque la pièce jointe est ouverte, elle fonctionne comme un lien vers l'emplacement de publication effectif du modèle. Le modèle de formulaire qui se trouve à cet emplacement est ce qui est effectivement ouvert dans l'éditeur InfoPath.
  
L’utilisation d’un modèle de formulaire au niveau du domaine envoyé en tant que pièce jointe de courrier électronique ressemble à tout autre type de document ; par exemple, un Microsoft Excel ou un document Microsoft Word document. Il suffit à l'utilisateur de cliquer sur le formulaire pour l'ouvrir et l'utiliser. Par ailleurs, tous les avantages des mises à jour du niveau Domaine sont accessibles aux utilisateurs.
  
Vous pouvez envoyer par courrier électronique des modèles de formulaire qui demandent l’accès Confiance totale, mais ces modèles doivent être signés, sinon ils ne seront pas autorisés à s’ouvrir. Les modèles de formulaire demandant un accès domaine ou restreint n’ont pas besoin d’être signés pour être envoyés en tant que pièce jointe d’un e-mail. InfoPath ne contrôle ni ne vérifie la signature, même si le modèle est signé, sauf pour vérifier s'il peut être mis à jour automatiquement. Vous pouvez signer numériquement un modèle de formulaire de type Domaine ou Restreint et continuer à disposer de la capacité de mise à jour automatique. Dans ce cas, la signature numérique empêche l'affichage de tout message d'avertissement de conflit en cache.
  
## <a name="sharing-forms-by-email-message-or-from-a-common-shared-location"></a>Partage de formulaires par message électronique ou à partir d’un emplacement partagé commun

Certaines questions doivent être posées lorsque vous créez un formulaire qui sera déployé par message électronique.
  
- **Votre formulaire sera-t-il mis à jour régulièrement ?** Si vous développez un formulaire devant être mis à jour régulièrement, celui-ci doit être publié sur un emplacement partagé avant d'être envoyé à d'autres utilisateurs. Cette méthode vous permet de mettre à jour le formulaire en en publiant des versions plus récentes sur l'emplacement partagé mais elle vous permet également de le distribuer immédiatement aux utilisateurs ne disposant pas d'un accès à l'emplacement partagé.

   Si un formulaire est mis à jour, puis distribué par message électronique, les utilisateurs obtiennent un message de conflit de cache lorsqu’ils tentent d’ouvrir le nouveau formulaire, s’ils disposent d’une version antérieure stockée sur leur ordinateur et que le chemin d’accès a changé. L'utilisateur sera invité à choisir la version du formulaire qu'il souhaite utiliser. Même si le formulaire mis à jour est identique à celui qui se trouve sur l'ordinateur de l'utilisateur, un message d'avertissement de conflit en cache sera tout de même affiché et l'utilisateur devra choisir la copie à utiliser. Il est recommandé dans ce cas de partager le formulaire depuis un emplacement partagé.

- **Votre formulaire a-t-il un accès à une connexion de données ou utilise-t-il des fonctionnalités non prises en charge au niveau de sécurité Restreint ?** Si vous développez un formulaire qui nécessite une sécurité de niveau Domaine, InfoPath exige que vous publiiez le formulaire sur un emplacement partagé pour permettre aux utilisateurs de l'ouvrir. Étant donné que les modèles de formulaire s’ouvrent uniquement au niveau de sécurité qu’ils demandent, les formulaires ouverts directement à partir d’un message électronique ne s’ouvrent pas si InfoPath ne peut pas accorder de sécurité au niveau du domaine.

## <a name="benefits-of-using-signed-form-templates"></a>Avantages de l’utilisation de modèles de formulaire signés

- La signature permet au modèle de formulaire de s'ouvrir avec un niveau de sécurité Confiance totale.

- Elle évite l'affichage du message de conflit en cache lorsque le formulaire est déplacé vers un nouvel emplacement.

De plus, si un modèle de formulaire est signé, vous bénéficiez également de la fonctionnalité de mise à jour automatique. Pour plus d'informations, consultez [Déploiement de modèles de formulaire signés](deploying-signed-infopath-form-templates.md).
  
### <a name="example-updating-domain-or-restricted-templates"></a>Exemple : mise à jour de modèles de domaine ou restreints

L'exemple suivant montre de quelle manière un modèle de formulaire mis à jour et signé demandant un accès Domaine ou Restreint peut remplacer une copie plus ancienne :
  
1. « A » envoie un modèle de formulaire signé à « B ».

2. « B » ouvre le modèle de formulaire.

3. « A » met à jour le modèle de formulaire (par exemple, en y ajoutant des champs).

4. « A » envoie le modèle de formulaire mis à jour à « B ».

5. « B » ouvre le modèle de formulaire mis à jour.

### <a name="example-deploying-restricted-form-templates-on-an-extranet"></a>Exemple : déploiement de modèles de formulaire restreints sur un extranet
  
1. Enregistrez le modèle de formulaire Domaine sur un site web qui exécute Microsoft SharePoint Foundation 2010.

2. Changez le niveau de sécurité du modèle de formulaire en Restreint.

3. Enregistrez le modèle de formulaire sur le Bureau de votre ordinateur.

4. Supprimez l'URL (requis uniquement si les utilisateurs ont accès à l'emplacement de publication d'origine).

5. Envoyez le formulaire aux utilisateurs sur un extranet.

6. Demandez-leur d'installer le formulaire.

7. Demandez-leur ensuite de vous renvoyer le formulaire après l'avoir rempli.

8. Enregistrez de nouveau le formulaire sur le site web qui exécute SharePoint Foundation 2010 et resserre le lien du formulaire à l’aide de l’option **Reconnecter les documents** à cette bibliothèque dans la page Paramètres bibliothèque **de formulaires**.

## <a name="signature-verification-failure"></a>Échec de vérification de signature

Un modèle de formulaire signé qui demande l'accès Confiance totale mais dont la signature ne peut être authentifiée ne sera pas ouvert. La vérification de signature peut échouer pour l'une des raisons suivantes :
  
- Le certificat racine ne se trouve pas dans le magasin de certificats principal approuvé.

- Le certificat qui a été utilisé pour signer le modèle de formulaire a expiré.

- Le certificat qui a été utilisé pour signer le modèle de formulaire a été révoqué.

- La signature du modèle de formulaire est endommagée (une indication que le modèle de formulaire a été modifié après avoir été signé).

Si un modèle de formulaire signé demande un accès Domaine ou Restreint, InfoPath ne contrôle ni ne vérifie la signature, sauf pour vérifier s'il peut être mis à jour automatiquement.
  
## <a name="infrastructure-registry-keys-for-form-migration-open-behavior"></a>Clés de Registre d’infrastructure pour le comportement d’ouverture de migration de formulaire

Lorsqu'un utilisateur essaie d'ouvrir un formulaire, et que le formulaire est identifié comme correspondant à un modèle de formulaire par son ID, InfoPath affiche un message d'erreur si le modèle de formulaire présente un niveau de confiance Domaine et que le domaine ne correspond pas à l'attribut *href* du formulaire. Ce système empêche l'ouverture de formulaires n'ayant pas été créés explicitement à l'aide du modèle de formulaire.
  
InfoPath n'autorise pas la coexistence de modèles de formulaire portant le même ID de formulaire. Quatre clés de registre supplémentaires aident les administrateurs système à donner aux utilisateurs la possibilité d'autoriser l'ouverture du fichier XML par rapport à un modèle de formulaire. Ce système permet également aux administrateurs de définir le comportement d'ouverture de leur choix pour les formulaires.
  
La table suivante décrit les paramètres par défaut des clés de registre. En l'absence de ces clés de registre, la valeur par défaut spécifiée dans la table entre en vigueur.
  
Les valeurs Nom correspondent aux paramètres de domaine Internet Explorer. Ces valeurs déterminent le comportement d'ouverture du formulaire dans ces zones de sécurité, soit en bloquant ou en autorisant l'ouverture du formulaire, soit en donnant à l'utilisateur la possibilité d'ouvrir le formulaire.
  
|**Valeur de nom**|**Bloquer**|**Interface utilisateur**|**Allow**|
|:-----|:-----|:-----|:-----|
|**Internet** <br/> |X  <br/> |||
|**Intranet** <br/> ||X  <br/> ||
|**Ordinateur client** <br/> |||X  <br/> |
|**Site approuvé** <br/> |||X  <br/> |

Le chemin d’accès à la clé de Registre est `HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\InfoPath\Open Behaviors`.

Le comportement d'ouverture du formulaire est défini comme suit :
  
- `Block [REG_DWORD = 0]`- Un dialogue d'erreur doté d'un bouton Aide apparaît. InfoPath n'autorise pas le fichier XML à s'ouvrir lorsque le formulaire est exécuté dans la zone de sécurité spécifiée et qu'il ne correspond pas au domaine du modèle.

- `User Interface [REG_DWORD = 1]`- La boîte de dialogue Oui/Non apparaît. InfoPath invite l'utilisateur à ouvrir le fichier XML par rapport au modèle de formulaire lorsque le formulaire est exécuté dans la zone de sécurité spécifiée et qu'il ne correspond pas au domaine du modèle.

- `Allow [REG_DWORD = 2]`- Le fichier XML s'ouvre sans message d'erreur ou d'avertissement. InfoPath autorise le fichier XML à s'ouvrir lorsque le formulaire est exécuté dans la zone de sécurité spécifiée et qu'il ne correspond pas au domaine du modèle.

Si un formulaire est ouvert par rapport à un modèle de formulaire exécuté au niveau de sécurité Domaine, et que le domaine de sécurité de l'emplacement « en cache à partir de » du modèle (c'est-à-dire, l'emplacement à partir duquel le formulaire est mis en cache) et que l'attribut **href** du formulaire ne correspond pas, InfoPath consulte le registre afin de définir le comportement d'ouverture du formulaire. Le comportement autorisé est basé sur la zone de sécurité où se trouve le modèle (la valeur *CachedFromLocation*).
  
Par exemple, lorsqu'un formulaire correspond à un modèle de formulaire basé sur un ID de formulaire mais pas sur un chemin d'accès, et que le modèle du formulaire est mis en cache depuis un emplacement Internet, InfoPath affiche un dialogue d'erreur doté d'un bouton d'aide.
  
> [!NOTE]
> [!REMARQUE] Étant donné que les formulaires InfoPath ne s'ouvrent pas lorsque le domaine est un domaine Internet Explorer de type Restreint, il n'y a pas de clé de registre pour les sites Internet Explorer de type Restreint.

  