---
title: Création de modèles de formulaires InfoPath fonctionnant avec InfoPath Forms Services
manager: soliver
ms.date: 03/20/2015
ms.audience: Developer
keywords:
- browser-compatible form templates [infopath 2007],forms [InfoPath 2007], browser-compatible,browser-compatible forms [InfoPath 2007],form templates [InfoPath 2007], browser-compatible,InfoPath 2007, browser-compatible forms,business logic, InfoPath Forms Services,InfoPath Forms Services, creating forms,InfoPath Forms Services, supported object model members,InfoPath Forms Services, supported classes and members
ms.localizationpriority: medium
ms.assetid: 7bd4fbbb-49c6-46a1-9584-895e5aa9a772
description: Les formulaires compatibles avec le navigateur déployés sur Microsoft SharePoint Server 2013 avec InfoPath Forms Services prise en charge des fonctionnalités et des contrôles qui couvrent la plupart des scénarios d’utilisation des formulaires InfoPath. Toutefois, les formulaires compatibles avec le navigateur, fournis par InfoPath Forms Services, ne prennent pas en charge toutes les fonctionnalités InfoPath. Certaines fonctionnalités et certains contrôles ne sont pas implémentés sur le serveur. D'autres fonctionnalités n'ont pas une représentation significative sur le serveur.
ms.openlocfilehash: 043171f917720997cc01947ce451661b8d286a48
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592968"
---
# <a name="creating-infopath-form-templates-that-work-with-infopath-forms-services"></a>Création de modèles de formulaires InfoPath fonctionnant avec InfoPath Forms Services

Les formulaires compatibles avec le navigateur déployés sur Microsoft SharePoint Server 2013 avec InfoPath Forms Services prise en charge des fonctionnalités et des contrôles qui couvrent la plupart des scénarios d’utilisation des formulaires InfoPath. Toutefois, les formulaires compatibles avec le navigateur, fournis par InfoPath Forms Services, ne prennent pas en charge toutes les fonctionnalités InfoPath. Certaines fonctionnalités et certains contrôles ne sont pas implémentés sur le serveur. D'autres fonctionnalités n'ont pas une représentation significative sur le serveur.
  
Les sections qui suivent spécifient les fonctionnalités prises en charge dans les formulaires compatibles avec le navigateur, celles qui ne peuvent pas être utilisées dans ce type de formulaire, ainsi que les fonctionnalités qui peuvent être spécifiées pour les formulaires compatibles avec le navigateur mais qui ne fonctionnent pas dans un navigateur Web.
  
## <a name="features-supported-by-both-infopath-and-infopath-forms-services"></a>Fonctionnalités prises en charge par InfoPath et InfoPath Forms Services

Les sections suivantes présentent la liste des fonctionnalités prises en charge par les modèles de formulaires compatibles avec le navigateur, déployés sur InfoPath Forms Services et pouvant s'ouvrir dans InfoPath et le navigateur.
  
### <a name="controls"></a>Contrôles

Les contrôles suivants sont pris en charge dans les modèles de formulaire qui peuvent être ouverts à la fois dans InfoPath et dans le navigateur.
  
- **Zone de texte**
    
- **Zone de texte enrichi** (modifiable uniquement dans Microsoft Internet Explorer) 
    
- **Zone de liste déroulante**
    
- **Zone de liste**
    
- **Sélecteur de dates** (Rendu sous la forme d'une zone de texte sur les navigateurs autres que Internet Explorer) 
    
- **Case à cocher**
    
- **Case d'option**
    
- **Bouton**
    
- **Section**
    
- **Section facultative**
    
- **Section extensible**
    
- **Tableau extensible**
    
- **Fichier joint**
    
- **Lien hypertexte**
    
- **Zone d'expression**
    
- **Zone de liste déroulante**
    
- **Zone de liste à sélection multiple**
    
- **Liste à puces**
    
- **Liste numéroée**
    
- **Liste simple**
    
- **Picture**
    
- **Groupe de choix**
    
- **Section de choix**
    
- **S sélectionneur de personnes/de groupes**
    
- **Sélecteur d'éléments externes**
    
- **Bouton Image**
    
- **Valeur calculée**
    
### <a name="declarative-features"></a>Fonctions déclaratives

Autres fonctions déclaratives fonctionnant dans InfoPath et le navigateur :
  
- Règles
    
- Calculs
    
- Validation
    
> [!NOTE]
> [!REMARQUE] Les règles, les calculs et les validations de données simples sont activés et exécutés dans le navigateur à l'aide de JScript. Les règles, les calculs et la validation de données complexes requièrent une publication préalable à l'exécution de ces opérations sur le serveur. 
  
### <a name="code"></a>Code

Le code de logique métier doit être basé sur le modèle objet InfoPath avec code managé, fourni par l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . Le code de logique métier exécuté sur le serveur est soumis aux restrictions suivantes : 
  
- Étant donné que chaque demande du serveur peut être gérée par un serveur frontal différent et que InfoPath Forms Services charge uniquement une seule instance de la logique métier, les programmeurs ne peuvent pas se baser sur les données stockées dans des variables globales ou statiques. Pour contourner cette restriction, la logique métier doit stocker les informations d'état dans un sac de propriétés accessible par l'intermédiaire de la propriété [FormState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.FormState.aspx) . 
    
- Un sous-ensemble des membres de l'espace de noms **Microsoft.Office.InfoPath** fournit des fonctionnalités, telles que la Gestion des droits relatifs à l'information (IRM), qui ne sont pas prises en charge sur le serveur. Pour plus d'information sur la prise en charge ou non des membres de modèle objet, voir Membres d'un modèle objet exécutables dans InfoPath et InfoPath Forms Services et Membres d'un modèle objet exécutables uniquement dans InfoPath, plus loin dans cette rubrique. 
    
- La logique métier écrite dans VBScript, JScript et le modèle objet compatible InfoPath 2003 fourni par les membres de l'espace de noms [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) ne sont pas pris en charge sur le serveur. 
    
## <a name="features-not-supported-by-infopath-forms-services"></a>Fonctionnalités non prises en charge par InfoPath Forms Services

Les sections suivantes décrivent les fonctionnalités non prises en charge par les modèles de formulaires compatibles avec le navigateur, déployés sur InfoPath Forms Services, pouvant s'ouvrir à la fois dans InfoPath et dans le navigateur.
  
Lorsque vous utilisez la fonctionnalité **Vérificateur de mise en page** en mode Création dans InfoPath pour confirmer la compatibilité avec InfoPath Forms Services, les fonctionnalités qui ne sont pas prises en charge génèrent des erreurs ou des messages. Les fonctionnalités qui génèrent des erreurs empêchent la publication du modèle de formulaire sous la forme d'un formulaire activé pour le navigateur. Les fonctionnalités qui génèrent des messages sont autorisées, mais cette fonctionnalité en particulier n'est pas exécutée lorsque le formulaire est ouvert dans un navigateur. 
  
### <a name="controls"></a>Contrôles

Les contrôles et les fonctionnalités de contrôle suivants ne sont pas pris en charge dans les modèles de formulaires qui peuvent être ouverts dans InfoPath et dans le navigateur.
  
- Filtres sur les contrôles extensibles
    
- **Maître/Détail**
    
- **Étiquette verticale**
    
- **Tableau extensible horizontal**
    
- **Image manuscrite**
    
- **Section récursive extensible**
    
### <a name="other-features-that-are-not-supported-or-not-fully-supported-by-infopath-forms-services"></a>Autres fonctionnalités non prises en charge en totalité ou en partie par InfoPath Forms Services

Autres fonctionnalités non prises en charge sur InfoPath Forms Services :
  
- Contrôles ActiveX
    
- Volets Office HTML
    
- Texte de l'espace réservé dans les contrôles. Par exemple, « Cliquez ici pour entrer un texte » (aucun texte n'est affiché dans le navigateur)
    
- Les connexions aux données de bases de données sont limitées à un accès en lecture seule aux bases de données SQL Server
    
- Rôles des utilisateurs
    
- Extensibilité des signatures numériques à travers le modèle objet. La signature numérique sur le serveur est prise en charge par l'intermédiaire d'un contrôle ActiveX qui s'exécute uniquement dans Microsoft Internet Explorer.
    
- Intégration HWS (Human Workflow Services). HWS a été désapprouvé par le serveur BizTalk
    
- Substitution des messages d'erreur du schéma XML. Cette fonctionnalité est rarement utilisée. Elle permet au concepteur de formulaires de fournir un message différent de celui fourni par MSXML ou **System.Xml** lorsqu'un document n'est pas validé (généralement, en raison d'une incompatibilité de type). Cette fonctionnalité n'est pas prise en charge dans l'interface utilisateur du concepteur et requiert une modification manuelle du fichier de définition du formulaire (.xsf). 
    
### <a name="features-with-no-direct-parallel-on-the-infopath-forms-services"></a>Fonctionnalités sans équivalences directes dans InfoPath Forms Services

Autres fonctionnalités non prises en charge dans InfoPath Forms Services :
  
- Boîtes de dialogue contextuelles au cours d'une validation non modale
    
- Intégration d'Outlook
    
- Compléments COM
    
- Fusionner les formulaires
    
- Enregistrement automatique, détection de panne et récupération
    
- Enveloppe électronique
    
- Exporter vers Excel
    
- Fonctionnalités Tablette / Écriture manuscrite, y compris le contrôle **Image manuscrite** 
    
- Annuler / Rétablir
    
- Gestion des droits relatifs à l'information (IRM)
    
- Boîtes de dialogue modales à partir de la logique métier
    
- Extensibilité XSLT (blocs **xd:preserve**) 
    
- Automatisation externe
    
- Mise en case des requêtes hors connexion
    
- Vérification de l'orthographe
    
- Mode de sécurité restreinte
    
> [!NOTE]
> Ces fonctionnalités ne génèrent aucune notification d'erreur ou message lorsque la fonctionnalité **Vérificateur de mise en page** est utilisée dans InfoPath en mode Création. 
  
## <a name="object-model-members-that-work-in-both-infopath-and-infopath-forms-services"></a>Membres du modèle objet travaillant à la fois dans InfoPath et dans InfoPath Forms Services

InfoPath fournit un nouveau modèle objet avec code managé intégrant un ensemble principal de fonctionnalités destinées à créer une logique métier personnalisée dans les modèles de formulaires. Une fois déployée dans SharePoint Server 2010 avec InfoPath Forms Services, la logique métier créée à partir de ce nouveau modèle objet s'exécutera à la fois dans un navigateur Web et dans InfoPath. Vous pouvez éventuellement écrire une logique métier plus élaborée qui, s'appuyant sur les possibilités de ce modèle objet, s'exécutera uniquement dans les modèles de formulaires ouverts pour modification dans InfoPath.
  
Pour écrire une logique métier exécutée à l'ouverture d'un formulaire dans un navigateur Web et dans InfoPath, activez la case à cocher **Activer les fonctions compatibles avec le navigateur uniquement** dans la boîte de dialogue **Créer un modèle de formulaire**, lors de la création d'un modèle de formulaire. Pour écrire une logique métier qui utilisera les fonctionnalités supplémentaires uniquement lorsqu'elle est ouverte dans InfoPath, désactivez la case à cocher **Activer les fonctions compatibles avec le navigateur uniquement** lors de la création d'un modèle de formulaire. Vous pouvez également modifier ce paramètre après avoir créé un modèle de formulaire en cliquant sur **Modifier les paramètres de compatibilité** dans le volet Office **Vérificateur de mise en page**, puis en activant ou en désactivant la case **Créer un modèle de formulaire qui peut être ouvert dans un navigateur ou dans InfoPath**. Si vous choisissez de créer un modèle de formulaire compatible avec le navigateur, le compilateur affiche une erreur si vous avez utilisé des classes ou des membres non compatibles avec InfoPath Forms Services. 
  
> [!NOTE]
> [!REMARQUE] Après la publication d'un modèle de formulaire activé pour le navigateur avec code managé dans SharePoint Server 2010 avec InfoPath Forms Services ou dans un emplacement partagé, le modèle de formulaire doit être téléchargé et approuvé par l'administrateur du serveur, avant d'être autorisé à être exécuté. 
  
Les classes et les membres suivants du modèle objet InfoPath avec code managé fourni par l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) sont pris en charge à la fois dans InfoPath et dans InfoPath Forms Services. 
  
|**Classe parent**|**Membres**|
|:-----|:-----|
|[AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx) <br/> |
||[Command](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Command.aspx) <br/> |
||[Connection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Connection.aspx) <br/> |
||[Timeout](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Timeout.aspx) <br/> |
||[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx) <br/> |
||[Command](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.Command.aspx) <br/> |
||[Connection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.Connection.aspx) <br/> |
||[Timeout](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.Timeout.aspx) <br/> |
|[Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) <br/> |[Environnement](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) <br/> |
||[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) <br/> |
||[Utilisateur](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.User.aspx) <br/> |
|[ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) <br/> |[Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) <br/> |
|[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |[ControlId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.ControlId.aspx) <br/> |
||[Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx) <br/> |
|[ControlEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ControlEvents.aspx) <br/> |[Élément](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ControlEvents.Item.aspx) <br/> |
|[DataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.Execute.aspx) <br/> |
||[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.Name.aspx) <br/> |
|[DataConnectionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.GetEnumerator.aspx) <br/> |
||[Élément](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.Item.aspx) <br/> |
||[Élément](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.Item.aspx) <br/> |
|[DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |[CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) <br/> |
||[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) <br/> |
||[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.Name.aspx) <br/> |
||[QueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.QueryConnection.aspx) <br/> |
||[ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.ReadOnly.aspx) <br/> |
||[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) <br/> |
|[DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.GetEnumerator.aspx) <br/> |
||[Élément](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx) <br/> |
||[Élément](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx) <br/> |
|[EmailAttachmentType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailAttachmentType.aspx) <br/> |[Aucune](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailAttachmentType.None.aspx) <br/> |
||[Xml](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailAttachmentType.Xml.aspx) <br/> |
||[XmlXsn](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailAttachmentType.XmlXsn.aspx) <br/> |
|[EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |[AttachmentFileName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.AttachmentFileName.aspx) <br/> |
||[Bcc](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Bcc.aspx) <br/> |
||[CC](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.CC.aspx) <br/> |
||[EmailAttachmentType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.EmailAttachmentType.aspx) <br/> |
||[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx) <br/> |
||[Introduction](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Introduction.aspx) <br/> |
||[Objet](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Subject.aspx) <br/> |
||[To](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.To.aspx) <br/> |
|[Environnement](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) <br/> |[IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) <br/> |
||[IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) <br/> |
|[EventManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EventManager.aspx) <br/> |[ControlEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EventManager.ControlEvents.aspx) <br/> |
||[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EventManager.FormEvents.aspx) <br/> |
||[XmlEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EventManager.XmlEvents.aspx) <br/> |
|[FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx) <br/> |
||[FileLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.FileLocation.aspx) <br/> |
|[FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx) <br/> |
||[Filename](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Filename.aspx) <br/> |
||[FolderUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.FolderUrl.aspx) <br/> |
|[FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |[DetailedMessage](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.DetailedMessage.aspx) <br/> |
||[FormErrorType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.FormErrorType.aspx) <br/> |
||[Message](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Message.aspx) <br/> |
||[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Name.aspx) <br/> |
||[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) <br/> |
|[FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) <br/> |
||[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) <br/> |
||[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Count.aspx) <br/> |
||[Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Delete.aspx) <br/> |
||[Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Delete.aspx) <br/> |
||[DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.DeleteAll.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetEnumerator.aspx) <br/> |
||[GetErrors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetErrors.aspx) <br/> |
||[GetErrors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetErrors.aspx) <br/> |
||[Élément](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Item.aspx) <br/> |
|[FormErrorType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorType.aspx) <br/> |[SchemaValidation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorType.SchemaValidation.aspx) <br/> |
||[SystemGenerated](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorType.SystemGenerated.aspx) <br/> |
||[UserDefined](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorType.UserDefined.aspx) <br/> |
|[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.aspx) <br/> |[Chargement](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) <br/> |
||[Envoyer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) <br/> |
||[VersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.VersionUpgrade.aspx) <br/> |
||[ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) <br/> |
|[FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |[Manifeste](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) <br/> |
||[OpenFileFromPackage](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.OpenFileFromPackage.aspx) <br/> |
||[Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Uri.aspx) <br/> |
||[Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Version.aspx) <br/> |
|[LoadingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.CancelableArgs.aspx) <br/> |
||[InputParameters](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.InputParameters.aspx) <br/> |
||[SetDefaultView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.SetDefaultView.aspx) <br/> |
||[SetDefaultView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.SetDefaultView.aspx) <br/> |
|[SharepointListQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx) <br/> |
||[QueryThisFormOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.QueryThisFormOnly.aspx) <br/> |
||[SiteUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.SiteUrl.aspx) <br/> |
|[SubmitEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SubmitEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SubmitEventArgs.CancelableArgs.aspx) <br/> |
|[Utilisateur](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) <br/> |[LoginName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.LoginName.aspx) <br/> |
||[UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) <br/> |
|[VersionUpgradeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.CancelableArgs.aspx) <br/> |
||[DocumentVersion](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.DocumentVersion.aspx) <br/> |
||[FormTemplateVersion](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.FormTemplateVersion.aspx) <br/> |
|[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) <br/> |
|[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) <br/> |[Caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.Caption.aspx) <br/> |
||[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.Name.aspx) <br/> |
|[ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Count.aspx) <br/> |
||[Default](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Default.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.GetEnumerator.aspx) <br/> |
||[Initiales](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) <br/> |
||[Élément](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Item.aspx) <br/> |
||[Élément](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Item.aspx) <br/> |
||[SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) <br/> |
||[SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) <br/> |
|[WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx) <br/> |
||[GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx) <br/> |
||[ServiceUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.ServiceUrl.aspx) <br/> |
||[SoapAction](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.SoapAction.aspx) <br/> |
||[Timeout](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Timeout.aspx) <br/> |
||[WsdlUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.WsdlUrl.aspx) <br/> |
|[XmlEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.aspx) <br/> |[Modifié](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) <br/> |
||[RaiseUndoRedoForChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.RaiseUndoRedoForChanged.aspx) <br/> |
||[Validation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) <br/> |
|[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |[Match](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Match.aspx) <br/> |
||[NewValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.NewValue.aspx) <br/> |
||[OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx) <br/> |
||[OldValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldValue.aspx) <br/> |
||[Opération](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Operation.aspx) <br/> |
||[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) <br/> |
||[UndoRedo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.UndoRedo.aspx) <br/> |
|[XmlEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvents.aspx) <br/> |[Élément](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvents.Item.aspx) <br/> |
||[Élément](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvents.Item.aspx) <br/> |
|[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |[CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) <br/> |
||[DataConnections](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx) <br/> |
||[DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) <br/> |
||[Erreurs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx) <br/> |
||[FormState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.FormState.aspx) <br/> |
||[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) <br/> |
||[NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) <br/> |
||[New](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.New.aspx) <br/> |
||[NotifyHost](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NotifyHost.aspx) <br/> |
||[QueryDataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.QueryDataConnection.aspx) <br/> |
||[ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ReadOnly.aspx) <br/> |
||[Signé](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) <br/> |
||[Envoyer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx) <br/> |
||[Template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx) <br/> |
||[Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Uri.aspx) <br/> |
||[ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) <br/> |
||[XmlLang](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.XmlLang.aspx) <br/> |
|[XmlFormCancelEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.aspx) <br/> |[Message](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.Message.aspx) <br/> |
||[MessageDetails](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.MessageDetails.aspx) <br/> |
|[XmlOperation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.aspx) <br/> |[Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.Delete.aspx) <br/> |
||[Insert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.Insert.aspx) <br/> |
||[Aucune](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.None.aspx) <br/> |
||[ValueChange](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.ValueChange.aspx) <br/> |
|[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) <br/> |
||[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) <br/> |
||[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) <br/> |
|[XPathTypedValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XPathTypedValue.aspx) <br/> |[Evaluate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XPathTypedValue.Evaluate.aspx) <br/> |
||[SetStringValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XPathTypedValue.SetStringValue.aspx) <br/> |
||[ToString](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XPathTypedValue.ToString.aspx) <br/> |
||[XPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XPathTypedValue.XPath.aspx) <br/> |
   
## <a name="object-model-members-that-work-only-in-infopath"></a>Membres du modèle objet fonctionnant uniquement dans InfoPath

Les classes et les membres suivants du modèle objet InfoPath avec code managé, fourni par l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) sont uniquement pris en charge dans InfoPath. 
  
> [!NOTE]
> [!REMARQUE] Ces membres du modèle objet peuvent être utilisés dans le code d'un modèle de formulaire activé pour le navigateur, lorsque vous écrivez une logique conditionnelle qui détermine si le formulaire est ouvert dans le navigateur ou dans InfoPath. Pour plus d’informations, [voir Write Conditional Logic That Determines the Run-time Environment](how-to-write-conditional-logic-that-determines-the-run-time-environment.md). 
  
|**Classe parent**|**Membres**|
|:-----|:-----|
|[ActionType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.aspx) <br/> |[Copier](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.Copy.aspx) <br/> |
||[Cut](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.Cut.aspx) <br/> |
||[Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.Delete.aspx) <br/> |
||[Paste](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.Paste.aspx) <br/> |
||[XCollectionInsert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionInsert.aspx) <br/> |
||[XCollectionInsertAfter](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionInsertAfter.aspx) <br/> |
||[XCollectionInsertBefore](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionInsertBefore.aspx) <br/> |
||[XCollectionRefreshFilter](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionRefreshFilter.aspx) <br/> |
||[XCollectionRemove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionRemove.aspx) <br/> |
||[XCollectionRemoveAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionRemoveAll.aspx) <br/> |
||[XFileAttachmentAttach](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XFileAttachmentAttach.aspx) <br/> |
||[XFileAttachmentOpen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XFileAttachmentOpen.aspx) <br/> |
||[XFileAttachmentRemove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XFileAttachmentRemove.aspx) <br/> |
||[XFileAttachmentSaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XFileAttachmentSaveAs.aspx) <br/> |
||[XOptionalInsert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XOptionalInsert.aspx) <br/> |
||[XOptionalRemove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XOptionalRemove.aspx) <br/> |
||[XReplaceReplace](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XReplaceReplace.aspx) <br/> |
|[Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) <br/> |[ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.ActiveWindow.aspx) <br/> |
||[CacheFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.CacheFormTemplate.aspx) <br/> |
||[ComAddIns](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.ComAddIns.aspx) <br/> |
||[GetFormTemplateLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.GetFormTemplateLocation.aspx) <br/> |
||[IsDestinationReachable](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.IsDestinationReachable.aspx) <br/> |
||[LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) <br/> |
||[MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) <br/> |
||[Quit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Quit.aspx) <br/> |
||[Quit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Quit.aspx) <br/> |
||[RegisterFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.RegisterFormTemplate.aspx) <br/> |
||[RegisterFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.RegisterFormTemplate.aspx) <br/> |
||[UnregisterFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.UnregisterFormTemplate.aspx) <br/> |
||[UsableHeight](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.UsableHeight.aspx) <br/> |
||[UsableWidth](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.UsableWidth.aspx) <br/> |
||[Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) <br/> |
||[Windows](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Windows.aspx) <br/> |
||[XmlForms](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.XmlForms.aspx) <br/> |
|[Certificat](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) <br/> |[ExpirationDate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.ExpirationDate.aspx) <br/> |
||[IssuedBy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.IssuedBy.aspx) <br/> |
||[IssuedTo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.IssuedTo.aspx) <br/> |
||[État](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.Status.aspx) <br/> |
|[CertificateStatus](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.aspx) <br/> |[Erreur](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.Error.aspx) <br/> |
||[Expiré](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.Expired.aspx) <br/> |
||[NotTrusted](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.NotTrusted.aspx) <br/> |
||[Revoked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.Revoked.aspx) <br/> |
||[Valid](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.Valid.aspx) <br/> |
|[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |[ChangeType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.ChangeType.aspx) <br/> |
||[Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx) <br/> |
||[UndoRedo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.UndoRedo.aspx) <br/> |
|[ErrorMode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ErrorMode.aspx) <br/> |[Modal](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ErrorMode.Modal.aspx) <br/> |
||[Modeless](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ErrorMode.Modeless.aspx) <br/> |
|[ExportFormat](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ExportFormat.aspx) <br/> |[Mht](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ExportFormat.Mht.aspx) <br/> |
||[Pdf](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ExportFormat.Pdf.aspx) <br/> |
||[Xps](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ExportFormat.Xps.aspx) <br/> |
|[FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |[ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.ErrorCode.aspx) <br/> |
|[FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) <br/> |
||[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) <br/> |
|[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.aspx) <br/> |[ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) <br/> |
||[Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) <br/> |
||[Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) <br/> |
||[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> |
|[FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |[CacheId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.CacheId.aspx) <br/> |
|[HtmlTaskPane](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.HtmlTaskPane.aspx) <br/> |[HtmlDocument](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.HtmlTaskPane.HtmlDocument.aspx) <br/> |
||[HtmlWindow](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.HtmlTaskPane.HtmlWindow.aspx) <br/> |
||[Naviguer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.HtmlTaskPane.Navigate.aspx) <br/> |
|[MachineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MachineState.aspx) <br/> |[IEInOfflineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MachineState.IEInOfflineState.aspx) <br/> |
||[Offline](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MachineState.Offline.aspx) <br/> |
||[Online](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MachineState.Online.aspx) <br/> |
|[MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.aspx) <br/> |[Disponible](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.Available.aspx) <br/> |
||[Bcc](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.Bcc.aspx) <br/> |
||[CC](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.CC.aspx) <br/> |
||[EmailAttachmentType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.EmailAttachmentType.aspx) <br/> |
||[Introduction](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.Introduction.aspx) <br/> |
||[Objet](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.Subject.aspx) <br/> |
||[To](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.To.aspx) <br/> |
||[Visible](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.Visible.aspx) <br/> |
|[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.CancelableArgs.aspx) <br/> |
||[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Count.aspx) <br/> |
||[Index](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Index.aspx) <br/> |
||[Rollback](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Rollback.aspx) <br/> |
||[Xml](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx) <br/> |
|[Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) <br/> |[ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx) <br/> |
||[DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx) <br/> |
||[Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx) <br/> |
||[PermissionFromPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PermissionFromPolicy.aspx) <br/> |
||[PolicyDescription](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyDescription.aspx) <br/> |
||[PolicyName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyName.aspx) <br/> |
||[RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx) <br/> |
||[StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx) <br/> |
||[UserPermissions](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.UserPermissions.aspx) <br/> |
|[PermissionType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.aspx) <br/> |[Remplacez](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Change.aspx) <br/> |
||[Edit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Edit.aspx) <br/> |
||[Extraire](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Extract.aspx) <br/> |
||[Contrôle total](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.FullControl.aspx) <br/> |
||[ObjectModel](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.ObjectModel.aspx) <br/> |
||[Print](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Print.aspx) <br/> |
||[Read](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Read.aspx) <br/> |
||[Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Save.aspx) <br/> |
||[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.View.aspx) <br/> |
|[SaveEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.CancelableArgs.aspx) <br/> |
||[CloseIfSaveCancelled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveCancelEventArgs.CloseIfSaveCancelled.aspx) <br/> |
||[Filename](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.Filename.aspx) <br/> |
||[IsSaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.IsSaveAs.aspx) <br/> |
||[PerformSaveOperation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.PerformSaveOperation.aspx) <br/> |
|[Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |[Certificat](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Certificate.aspx) <br/> |
||[Comment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Comment.aspx) <br/> |
||[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) <br/> |
||[SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx) <br/> |
||[État](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Status.aspx) <br/> |
|[SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.Count.aspx) <br/> |
||[CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.GetEnumerator.aspx) <br/> |
||[Élément](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.Item.aspx) <br/> |
|[SignatureRelation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureRelation.aspx) <br/> |[Cosigner](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureRelation.Cosign.aspx) <br/> |
||[CounterSign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureRelation.CounterSign.aspx) <br/> |
||[Single](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureRelation.Single.aspx) <br/> |
|[SignatureStatus](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureStatus.aspx) <br/> |[Erreur](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureStatus.Error.aspx) <br/> |
||[Invalid](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureStatus.Invalid.aspx) <br/> |
||[Unsupported](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureStatus.Unsupported.aspx) <br/> |
||[Valid](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureStatus.Valid.aspx) <br/> |
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |[Caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Caption.aspx) <br/> |
||[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Name.aspx) <br/> |
||[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) <br/> |
||[SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx) <br/> |
||[SignatureRelation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureRelation.aspx) <br/> |
||[Signatures](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx) <br/> |
||[XPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.XPath.aspx) <br/> |
|[SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.GetEnumerator.aspx) <br/> |
||[Élément](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.Item.aspx) <br/> |
||[ShowSignatureDialog](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.ShowSignatureDialog.aspx) <br/> |
|[SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) <br/> |[SignatureWizard](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignatureWizard.aspx) <br/> |
||[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignedDataBlock.aspx) <br/> |
|[TaskPane](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPane.aspx) <br/> |[TaskPaneType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPane.TaskPaneType.aspx) <br/> |
||[Visible](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPane.Visible.aspx) <br/> |
|[TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.GetEnumerator.aspx) <br/> |
||[Élément](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.Item.aspx) <br/> |
||[Élément](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.Item.aspx) <br/> |
|[TaskPaneType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.aspx) <br/> |[BulletsNumbering](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.BulletsNumbering.aspx) <br/> |
||[ClipArt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.ClipArt.aspx) <br/> |
||[Find](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.Find.aspx) <br/> |
||[Mise en forme](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.Formatting.aspx) <br/> |
||[Html](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.Html.aspx) <br/> |
||[ParagraphFormatting](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.ParagraphFormatting.aspx) <br/> |
||[Replace](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.Replace.aspx) <br/> |
||[Orthographe](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.Spelling.aspx) <br/> |
|[Utilisateur](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) <br/> |[IsUserMemberOf](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.IsUserMemberOf.aspx) <br/> |
|[UserPermission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.aspx) <br/> |[ExpirationDate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.ExpirationDate.aspx) <br/> |
||[Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Permission.aspx) <br/> |
||[Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Remove.aspx) <br/> |
||[UserId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.UserId.aspx) <br/> |
|[UserPermissionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.aspx) <br/> |[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) <br/> |
||[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) <br/> |
||[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) <br/> |
||[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) <br/> |
||[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.GetEnumerator.aspx) <br/> |
||[Élément](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Item.aspx) <br/> |
||[Élément](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Item.aspx) <br/> |
||[Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx) <br/> |
||[RemoveAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.RemoveAll.aspx) <br/> |
|[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) <br/> |
||[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) <br/> |
||[ExecuteAction](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) <br/> |
||[ExecuteAction](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) <br/> |
||[Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) <br/> |
||[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) <br/> |
||[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) <br/> |
||[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) <br/> |
||[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) <br/> |
||[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) <br/> |
||[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) <br/> |
||[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) <br/> |
||[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) <br/> |
||[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) <br/> |
||[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) <br/> |
||[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) <br/> |
|[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) <br/> |[HideName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.HideName.aspx) <br/> |
|[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) <br/> |[Activate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Activate.aspx) <br/> |
||[Active](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Active.aspx) <br/> |
||[Caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Caption.aspx) <br/> |
||[Close](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx) <br/> |
||[Close](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx) <br/> |
||[CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) <br/> |
||[Height](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Height.aspx) <br/> |
||[Left](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Left.aspx) <br/> |
||[MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.MailEnvelope.aspx) <br/> |
||[TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.TaskPanes.aspx) <br/> |
||[Top](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Top.aspx) <br/> |
||[Width](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Width.aspx) <br/> |
||[WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowState.aspx) <br/> |
||[WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowType.aspx) <br/> |
||[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.XmlForm.aspx) <br/> |
|[WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.GetEnumerator.aspx) <br/> |
||[Élément](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Item.aspx) <br/> |
|[WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.aspx) <br/> |[Agrandi](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.Maximized.aspx) <br/> |
||[Réduit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.Minimized.aspx) <br/> |
||[Normal](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.Normal.aspx) <br/> |
|[WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) <br/> |[Designer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.Designer.aspx) <br/> |
||[Éditeur](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.Editor.aspx) <br/> |
|[XmlChangingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.CancelableArgs.aspx) <br/> |
|[XmlEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.aspx) <br/> |[Modification](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) <br/> |
|[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |[Close](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Close.aspx) <br/> |
||[Dirty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Dirty.aspx) <br/> |
||[Extension](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Extension.aspx) <br/> |
||[GetWorkflowTasks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTasks.aspx) <br/> |
||[GetWorkflowTemplates](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTemplates.aspx) <br/> |
||[Host](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Host.aspx) <br/> |
||[Hébergé](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Hosted.aspx) <br/> |
||[HostName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.HostName.aspx) <br/> |
||[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) <br/> |
||[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) <br/> |
||[Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx) <br/> |
||[Print](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) <br/> |
||[Print](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) <br/> |
||[Recovered](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Recovered.aspx) <br/> |
||[Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx) <br/> |
||[SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) <br/> |
||[SetSaveAsDialogFilename](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogFilename.aspx) <br/> |
||[SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogLocation.aspx) <br/> |
||[SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) <br/> |
||[TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.TaskPanes.aspx) <br/> |
||[UserRole](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.UserRole.aspx) <br/> |
|[XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Count.aspx) <br/> |
|[XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.GetEnumerator.aspx) <br/> |
||[Élément](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Item.aspx) <br/> |
||[New](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) <br/> |
||[New](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) <br/> |
||[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) <br/> |
||[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) <br/> |
||[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) <br/> |
||[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) <br/> |
||[Ouvert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) <br/> |
||[Ouvert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) <br/> |
|[XmlFormOpenMode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormOpenMode.aspx) <br/> |**XmlFormOpenMode.Default** <br/> |
||**XmlFormOpenMode.FailOnVersionMismatch** <br/> |
||**XmlFormOpenMode.FailOnVersionOlder** <br/> |
||**XmlFormOpenMode.IgnoreDataConnectionsFailure** <br/> |
||**XmlFormOpenMode.PromptIfSigned** <br/> |
||**XmlFormOpenMode.ReadOnly** <br/> |
||**XmlFormOpenMode.TransformEvenIfSigned** <br/> |
||**XmlFormOpenMode.UseExistingVersion** <br/> |
||**XmlFormOpenMode.UseFileConverter** <br/> |
|[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) <br/> |
   

