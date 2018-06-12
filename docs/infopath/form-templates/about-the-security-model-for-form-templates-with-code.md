---
title: Sur le modèle de sécurité pour les modèles de formulaires avec Code
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2007, security,code access security [InfoPath 2007],security [InfoPath 2007], security model for managed code,security [InfoPath 2007], levels,CAS [InfoPath 2007],InfoPath 2003-compatible form templates, security,permissions [InfoPath 2007]
localization_priority: Normal
ms.assetid: 5e1c1c72-f98d-4871-9c57-82c315277aa1
description: Les modèles de formulaires InfoPath avec code managé prennent en charge les mêmes niveaux de sécurité que le script exécuté dans les modèles de formulaires non managés, ainsi que les fonctionnalité supplémentaires de sécurité d'accès au code qui s'appliquent au code managé exécuté sous le Common Language Runtime (CLR) de .NET Framework.
ms.openlocfilehash: cfeb2117232d041cef43d282ff5aab482609f512
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782346"
---
# <a name="about-the-security-model-for-form-templates-with-code"></a>Sur le modèle de sécurité pour les modèles de formulaires avec Code

Les modèles de formulaires InfoPath avec code managé prennent en charge les mêmes niveaux de sécurité que le script exécuté dans les modèles de formulaires non managés, ainsi que les fonctionnalité supplémentaires de sécurité d'accès au code qui s'appliquent au code managé exécuté sous le Common Language Runtime (CLR) de .NET Framework.
  
## <a name="infopath-managed-object-model-security-levels"></a>Niveaux de sécurité du modèle objet managé d'InfoPath

Le tableau suivant décrit la relation entre les niveaux de sécurité pour les membres du modèle objet de script et le jeu d'autorisations correspondant exigé à chaque niveau lorsque le membre du modèle objet est utilisé dans un modèle de formulaire avec code managé.
  
|**Niveau de sécurité du modèle objet**|**Description**|**Jeu d’autorisations exigé**|
|:-----|:-----|:-----|
|0  <br/> |Accessible sans restrictions.  <br/> |Aucun  <br/> |
|2  <br/> |Accessible uniquement par les formulaires qui s'exécutent dans le même domaine que le formulaire ouvert ou par les formulaires qui disposent d'autorisations indépendantes des domaines.  <br/> |Aucun  <br/> |
|3  <br/> |Accessible uniquement par les formulaires disposant d'une autorisation totale.  <br/> |Autorisation totale  <br/> |
   
> [!NOTE]
> Le niveau de sécurité « 1 » n'est pas utilisé par le serveur COM d'InfoPath actuel et est réservé pour un usage ultérieur. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Bien que les niveaux 0 et 2 du modèle objet n'exigent aucun jeu d'autorisations parce qu'ils contiennent du code managé, ils se comportent tel que cela est défini pour le niveau de sécurité d'accès au domaine Domaine, décrit dans la section suivante. 
  
Le niveau de sécurité de chaque membre du modèle objet exposé par les assemblys Microsoft.Office.InfoPath et Microsoft.Office.Interop.InfoPath.SemiTrust est spécifié dans la section Remarques de la rubrique qui documente ce membre dans les espaces de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) et [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . 
  
## <a name="infopath-domain-access-security-levels"></a>Niveaux de sécurité d'accès au domaine InfoPath

Avec les niveaux de sécurité du modèle objet appliqués par le serveur COM exposé par l'application InfoPath, InfoPath définit trois niveaux de sécurité qui sont appliqués en fonction de l'emplacement du modèle de formulaire, de la manière dont le formulaire est déployé et de la configuration des paramètres en mode Création. Ces trois niveaux de sécurité sont définis dans le tableau suivant.
  
|**Niveau de sécurité d’accès au domaine**|**Description**|
|:-----|:-----|
|Restreint  <br/> |N’autorise pas les communications en dehors du modèle de formulaire. Ce niveau de sécurité permet d'éviter que les formulaires dangereux transmettent des données de votre ordinateur à un utilisateur malintentionné. Lors de l’exécution dans ce mode de sécurité, les fonctionnalités suivantes ne fonctionneront pas : volet de tâches personnalisé, les connexions de données (sauf l’envoi de messagerie), les contrôles ActiveX, code de formulaire avec code managé, rôles et flux de travail. Gérés de formulaires avec code modèles ne peuvent pas être exécutées dans le domaine restreint. Lorsqu’un modèle de formulaire avec code managé est défini sur le paramètre **déterminer automatiquement le niveau de sécurité** dans la catégorie **sécurité et approbation** de la boîte de dialogue **Options de formulaire** , le modèle de formulaire toujours nécessite au moins l’accès de sécurité de domaine niveau d’exécuter du code.  <br/><br/>**IMPORTANT**: l’assembly de code managé créé pour un modèle de formulaire avec code managé n’est pas charger et exécuter lorsqu’un formulaire est ouvert à partir d’un domaine restreint, par exemple, à partir d’un formulaire InfoPath envoyé comme pièce jointe. Tout modèle de formulaire que vous souhaitez déployer en tant que pièce jointe doit ignorer les fonctionnalités répertoriées ci-dessus, et si le modèle de formulaire contient du code de formulaire, le code de formulaire doit être implémenté dans JScript ou VBScript et doit utiliser uniquement des membres du modèle objet avec un niveau de sécurité de 0 (zéro) .           |
|Domaine  <br/> |Restreint un formulaire en fonction de son emplacement dans une des zones de sécurité définies par Microsoft Internet Explorer. Par exemple, si le formulaire se trouve sur l'intranet local, il peut communiquer avec d'autres données à l'intérieur de son domaine, mais il n'est pas autorisé à récupérer des données provenant d'autres domaines. La présence dans une zone de sécurité Microsoft Internet Explorer détermine également si les contrôles ActiveX marqués comme n'étant pas sûrs pour les scripts sont autorisés à s'exécuter.  <br/> |
|Autorisation totale  <br/> |Permet d’exécuter un formulaire avec autorisation totale sur l’ordinateur où le formulaire sera utilisé. Ce niveau de sécurité peut uniquement être utilisé lorsque vous travaillez avec un formulaire est signé numériquement avec une signature qui correspond à un éditeur racine de confiance sur votre ordinateur, ou en créant un programme d’installation installe le formulaire et définit le **requireFullTrust** attribut de l’élément **xDocumentClass** « Oui » dans le fichier de définition du formulaire (.xsf). À l’aide de ce paramètre, votre formulaire peut accéder à des appels de modèle objet qui requièrent le niveau de sécurité du modèle objet 3, telles que les propriétés et méthodes qui accèdent à du système de fichiers, et vous pouvez désactiver certaines invites de sécurité qui s’affichent lors de l’exécution à une sécurité plus restrictive niveau.  <br/> |
   
Par défaut, un formulaire InfoPath est configuré pour sélectionnez automatiquement le niveau de sécurité restreint ou domaine selon les fonctionnalités qui sont utilisés dans le modèle de formulaire, et où et comment le modèle de formulaire est déployé. Par exemple, un modèle de formulaire déployé en tant que pièce jointe est automatiquement configuré au niveau de sécurité restreint. Le paramètre de sécurité est toujours aussi restrictif que possible, commençant à restreint pour garantir un meilleur niveau de protection de vos données. Lorsqu’un modèle de formulaire qui contient du code managé est défini sur Sélectionner automatiquement le niveau de sécurité, le modèle de formulaire toujours nécessite au moins le niveau d’accès de sécurité domaine avant l’exécution de code. Vous pouvez substituer manuellement ce paramètre au moment du design pour sélectionner un niveau de sécurité plus approprié pour le formulaire à l’aide de la procédure suivante. 
  
### <a name="specify-a-forms-security-level"></a>Définition du niveau de sécurité d'un formulaire

1. Ouvrez le formulaire dans le concepteur de formulaires InfoPath, cliquez sur l'onglet **Fichier**, cliquez sur **Informations**, puis cliquez sur **Options de formulaire**.
    
2. Dans la boîte de dialogue **Options de formulaire**, cliquez sur **Sécurité et approbation**. 
    
3. Désactivez la case à cocher **Déterminer automatiquement le niveau de sécurité (recommandé)**. 
    
4. Sélectionnez le niveau de sécurité souhaité.
    
> [!NOTE] 
> - Si vous choisissez le niveau de sécurité **Restreint** pour un modèle de formulaire avec code managé, le code du formulaire n'est pas chargé pas et ne s'exécute pas, quels que soient les membres du modèle objet utilisés dans le code du formulaire. Ce niveau de sécurité est principalement conçu pour les formulaires InfoPath sont déployés à l’aide de la messagerie.     
> - Si vous sélectionnez le niveau de sécurité **Autorisation totale**, vous devez signer numériquement le formulaire ou l'installer et l'inscrire. Pour plus d’informations, voir [Déployer des modèles de formulaire InfoPath avec Code](how-to-deploy-infopath-form-templates-with-code.md).
    
Le tableau suivant récapitule le modèle de sécurité d'InfoPath. La première colonne présente le niveau spécifié pour le formulaire ou le niveau requis. Les deuxième et troisième colonnes spécifient si l'emplacement du formulaire dispose d'un identificateur URN ou URL. Les autres colonnes spécifient les éléments autorisés à s'exécuter. Pour plus d'informations sur les scénarios de déploiement et les jeux d'autorisations pour les modèles de formulaires avec code managé, voir la section « Fonctionnalités de sécurité de l'accès au code du Common Language Runtime » plus loin dans cette rubrique.
  
|**Niveau requis par le formulaire**|**Possède un identificateur URN.**|**Est l’identificateur d’URL**|**ActiveX marqués comme non sécurisé pour les scripts**|**Accès entre domaines**|**Code managé**|**Sécurité du modèle objet**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Restreint  <br/> ||X   <br/> |Pas de ActiveX  <br/> |Échec  <br/> |Le formulaire se charge, mais le code managé ne s'exécute pas.  <br/> |0  <br/> |
|Domaine (zone Internet Explorer **sites sensibles** )  <br/> |Ne s'exécute pas du tout.  <br/> |Ne s'exécute pas du tout.  <br/> |Ne s'exécute pas du tout.  <br/> |Ne s'exécute pas du tout.  <br/> |Ne s'exécute pas du tout.  <br/> |Ne s'exécute pas du tout.  <br/> |
|Domaine (zone Internet Explorer **Internet** )  <br/> |X   <br/> ||Échec  <br/> |Échec  <br/> |Ne s'exécute pas du tout.  <br/> |0  <br/> |
|Domaine (zone Internet Explorer, **intranet Local** )  <br/> |X   <br/> ||Échec  <br/> |Invite  <br/> |Code managé s’exécute avec les autorisations **intranet Local** .  <br/> |2  <br/> |
|Domaine (zone Internet Explorer les **sites de confiance** )  <br/> |X   <br/> ||Invite  <br/> |OK  <br/> |Code managé s’exécute avec des autorisations **Internet** . Accès inter-domaines est autorisée. Notez que même si le formulaire est dans la zone **sites de confiance** , les autorisations de la zone **Internet** sont appliquées.  <br/> |2  <br/> |
|Domaine (zone Internet Explorer **ordinateur Local** )  <br/> |X   <br/> |X   <br/> |Invite  <br/> |Échec  <br/> |Code managé s’exécute avec les autorisations **intranet Local** .  <br/> |2  <br/> |
|Autorisation totale  <br/> |X   <br/> |X   <br/> |OK  <br/> |OK  <br/> |Autorisation totale  <br/> |3  <br/> |
   
> [!IMPORTANT]
> [!IMPORTANTE] Les descriptions ci-dessus dans les colonnes « ActiveX marqué comme non sûr pour les scripts » et « Accès entre domaines » utilisent les paramètres de sécurité par défaut de Microsoft Internet Explorer. Si un utilisateur modifie ses paramètres de sécurité, le comportement d'InfoPath est modifié en conséquence. Par exemple, si la zone **Intranet local**, **Accès aux sources de données sur plusieurs domaines** est définie sur l'option **Activer**, les utilisateurs ne peuvent pas autoriser un accès entre les domaines, tel que décrit dans le tableau. 
  
## <a name="common-language-runtime-code-access-security-features"></a>Fonctionnalités de sécurité de l'accès au code du Common Language Runtime

Lors de la compilation d'un modèle de formulaire InfoPath avec code managé, un assembly privé avec code managé contenant l'implémentation de la logique du code de formulaire est créé.
  
Dans .NET Framework, par défaut, un assembly de code managé dispose des autorisations totales lorsqu'il s'exécute sur l'ordinateur local, et il ne dispose pas de ces autorisations lorsqu'il s'exécute sur l'intranet. Pour un contrôle plus précis de la stratégie de sécurité, et pour offrir la possibilité d'exécuter des modèles de formulaires InfoPath avec code managé comme formulaires disposant d'une autorisation totale depuis l'intranet, InfoPath implémente l'architecture de sécurité suivante.
  
- L'application InfoPath héberge le CLR (Common Language Runtime) de .NET Framework.
    
- Dans le CLR d'InfoPath, chaque modèle de formulaire avec code managé s'exécute dans un domaine d'application distinct. Cet environnement permet l'isolement, le déchargement et les limites de sécurité nécessaires à l'exécution du code managé.
    
- InfoPath définit une stratégie de sécurité par défaut sur le domaine de l'application en fonction du niveau d'autorisation associé au modèle de formulaire et à l'URL de son emplacement.
    
- Par défaut, un modèle de formulaire avec code managé qui s'exécute sur l'ordinateur local (groupe de codes de la zone Poste de travail) obtient un jeu d'autorisations inférieur à l'Autorisation totale. Pour obtenir les autorisations totales, le formulaire doit être inscrit ou signé numériquement par un certificat approuvé.
    
La stratégie de sécurité par défaut définie pour le domaine d'application d'un modèle de formulaire avec code managé assure l'application des niveaux de sécurité d'accès au domaine InfoPath, ainsi que des restrictions de sécurité .NET supplémentaires. Pour une plus grande souplesse, le système de sécurité d'InfoPath reconnaît un groupe de codes de sécurité d'accès au code .NET appelé « Modèles de formulaires InfoPath ». Si ce groupe de code est présent sur l'ordinateur de l'utilisateur, sa configuration de sécurité, ainsi que celle de tous ses groupes de codes enfants, est appliquée au domaine de l'application.
  
> [!IMPORTANT] 
> - Le groupe de codes Modèles de formulaires InfoPath s'applique uniquement à l'assembly du code de formulaire managé. Ainsi, si vous accordez le jeu d'autorisations Autorisation totale au code de formulaire InfoPath avec code managé mais que vous n'avez pas installé et inscrit (ou signé numériquement) le formulaire lui-même (ce qui attribue l'autorisation totale à tout le modèle de formulaire), les appels effectués dans le code du formulaire à des membres du modèle objet du niveau de sécurité 3 échouent toujours.   
> - Si vous faites référence à un assembly configuré avec un jeu d'autorisations restreint à l'aide de Hash, Strong Name ou Publisher, ou que vous chargez explicitement un assembly (Assembly.Load) afin de déterminer son appartenance à un projet de modèle de formulaire, l'assembly est malgré tout chargé et exécuté par le modèle de formulaire.
    
Pour plus d’informations sur la façon de créer et configurer le groupe de codes modèles de formulaires InfoPath, voir [Configurer les paramètres de sécurité pour les modèles de formulaire avec du Code](how-to-configure-security-settings-for-form-templates-with-code.md).
  
Le tableau suivant récapitule les scénarios de déploiement et les jeux d'autorisations qui s'appliquent aux modèles de formulaires avec code managé.
  
|**Scénario de déploiement**|**Jeu d’autorisations**|**Remarques**|
|:-----|:-----|:-----|
|Le modèle de formulaire est publié sur l'ordinateur local et le développeur utilise Visual Studio pour écrire et déboguer le code du formulaire.  <br/> |Jeu d'autorisations intranet local  <br/> Les assemblys installés dans le Global Assembly Cache (GAC) et marqués avec l’attribut **AllowPartiallyTrustedCallersAttribute** sont accordées le jeu autorisation totale.  <br/> |Par défaut, les modèles de formulaire en cours d’exécution à partir de l’ordinateur local ne sont pas accordées le jeu autorisation totale. Alors que les membres qui nécessitent des autorisations de confiance totale du modèle de développement de modèles de formulaire qui utilisent les fonctionnalités et les appels vers un objet, vous pouvez utiliser la procédure décrite dans [l’Aperçu et déboguer les modèles de formulaires qui nécessitent une confiance totale](how-to-preview-and-debug-form-templates-that-require-full-trust.md).  <br/> |
|Le modèle de formulaire est publié sur l'ordinateur local et fait référence à un assembly personnalisé qui exige le jeu d'autorisations Autorisation totale sur l'ordinateur local.  <br/> |Jeu d'autorisations intranet local  <br/> Les assemblys installés dans le Global Assembly Cache (GAC) et marqués avec l’attribut **AllowPartiallyTrustedCallersAttribute** sont accordées le jeu autorisation totale. L’assembly personnalisé est accordé le jeu d’autorisations Intranet Local.  <br/> |Pour référencer des assemblys externes et les utiliser dans le code du modèle de formulaire, le développeur doit utiliser le groupe de codes Modèles de formulaires InfoPath pour accorder l'Autorisation totale (ou le jeu d'autorisations approprié) à l'assembly externe référencé dans le code du modèle de formulaire. InfoPath prend aucune décision quant aux assemblys externes autres que ceux installés dans le Global Assembly Cache (GAC). Le développeur doit accorder de manière explicite les autorisations nécessaires à l'aide du groupe de codes Modèles de formulaires InfoPath, même si l'assembly dispose déjà d'autorisations accordées dans le cadre du groupe de codes de la Zone Poste de travail.  <br/> |
|Le modèle de formulaire est publié dans un emplacement partagé sur l'intranet local, par exemple un partage de fichiers, une bibliothèque de formulaires SharePoint ou un serveur Web.  <br/> |Jeu d'autorisations Intranet local  <br/> Les assemblys installés dans le Global Assembly Cache (GAC) et marqués avec l’attribut **AllowPartiallyTrustedCallersAttribute** sont accordées le jeu autorisation totale.  <br/> ||
|Le modèle de formulaire est publié dans un emplacement partagé sur l'intranet local, par exemple un partage de fichiers, une bibliothèque de formulaires SharePoint ou un serveur Web désigné comme étant un site approuvé par Internet Explorer.  <br/> |Jeu d'autorisations Internet  <br/> Les assemblys signés par Microsoft et ECMA obtiennent le jeu Autorisation totale.  <br/> |La sécurité d'accès au code du CLR accorde uniquement le jeu d'autorisations Internet aux sites conçus comme Sites de confiance dans Internet Explorer. InfoPath respecte cette règle. Notez que ceci diffère d'un modèle de formulaire InfoPath qui utilise un script comme code, qui obtient un jeu d'autorisations plus élevé lorsqu'il est publié dans une zone Sites de confiance.   <br/> |
|Le modèle de formulaire est téléchargé ou copié depuis un emplacement Internet.  <br/> |Aucun par défaut. L'assembly de code managé du modèle de formulaire ne se charge pas et ne s'exécute pas.  <br/> ||
   
## <a name="see-also"></a>Voir aussi

- [Configurer les paramètres de sécurité pour les modèles de formulaires avec Code](how-to-configure-security-settings-for-form-templates-with-code.md)
- [Afficher un aperçu et déboguer les modèles de formulaires nécessitant la confiance totale](how-to-preview-and-debug-form-templates-that-require-full-trust.md)

