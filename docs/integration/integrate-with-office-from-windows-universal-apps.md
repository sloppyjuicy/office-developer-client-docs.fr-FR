---
title: Intégration à Office à partir d'applications universelles Windows
manager: soliver
ms.date: 02/06/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 60b4fa23-0075-4f6a-8bd0-9e53e99432d5
description: Vous pouvez intégrer vos applications tierces de plateforme d'application universelle Windows à Excel Mobile, PowerPoint Mobile et Word Mobile. Les applications universelles s'intègrent aux applications Office via les contrats de sélecteur de fichiers Windows, les propriétés Expando et les contrats de mise à jour des fichiers mis en cache.
ms.openlocfilehash: 3c61e5697fad8e79ca8c8a76843880fd79a842c3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596721"
---
# <a name="integrate-with-office-from-windows-universal-apps"></a>Intégration à Office à partir d’applications universelles Windows

Vous pouvez intégrer vos applications tierces de plateforme d'application universelle Windows à Excel Mobile, PowerPoint Mobile et Word Mobile. Les applications universelles s'intègrent aux applications Office via les [contrats de sélecteur de fichiers](https://msdn.microsoft.com/library/windows/apps/hh465174.aspx) Windows, les [propriétés Expando](https://msdn.microsoft.com/library/windows/apps/xaml/hh770655.aspx) et les [contrats de mise à jour des fichiers mis en cache](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.cachedfileupdater.aspx).
  
Lorsque vous intégrez votre application universelle à Excel, PowerPoint ou Word Mobile, vos utilisateurs peuvent ouvrir les documents Office fournis par votre application, que ce soit lorsqu'ils parcourent Office ou lorsqu'ils utilisent Windows pour ouvrir des fichiers dans votre application. Les utilisateurs peuvent également enregistrer le fichier dans votre application universelle, qui télécharge le fichier vers votre service.
  
Les fichiers ouverts de cette façon apparaissent dans la liste récente d'Office, afin que vos utilisateurs puissent facilement les trouver et les ouvrir à nouveau.
  
Cette intégration exige que votre application universelle :
    
- Implémente les [contrats de sélecteur de fichiers](https://msdn.microsoft.com/library/windows/apps/hh465174.aspx) Windows.
    
- représente un magasin de fichiers (par exemple, une application qui permet d’accéder au stockage cloud).
    
## <a name="expando-properties"></a>Propriétés Expando

Les applications universelles Windows peuvent utiliser des propriétés Expando pour communiquer des informations supplémentaires qui sont associées aux fichiers. Pour plus d'informations sur leur fonctionnement dans Windows, voir « System.ExpandoProperties » dans [StorageItemContentProperties.SavePropertiesAsync](https://msdn.microsoft.com/library/windows/apps/xaml/hh770655.aspx).
  
Le tableau suivant décrit les propriétés que votre application doit fournir à Office pour activer des scénarios de fichiers ouverts. Si cette information n'est pas indiquée, tous les fichiers de votre application sont ouverts en lecture seule. Les utilisateurs peuvent les ouvrir et les modifier en fonction du type de licence Office dont ils disposent, et du type de document qu'ils essaient d'ouvrir.
  
Définissez ces propriétés dans l'ensemble de propriétés **System.ExpandoProperties**. 
  
|**Propriété**|**Description**|**Type**|**Exemple**|
|:-----|:-----|:-----|:-----|
|**AppDisplayName** <br/> |Nom du fournisseur à afficher pour l'utilisateur. Il s'affiche à plusieurs endroits dans Office, comme la liste des documents récents.  <br/> |String  <br/> |Contoso  <br/> |
|**MicrosoftOfficeOwnershipType** <br/> |En ce qui concerne la gestion des licences, indiquez si le document/l'emplacement est personnel ou professionnel. Les valeurs autorisées sont 1 (personnel) et 2 (professionnel). Par exemple, si le fichier de votre utilisateur est stocké dans Contoso Business, utilisez la valeur « 2 » pour les documents professionnels.  <br/> |Unit32  <br/> | 1 ou 2  <br/> Par exemple, si le fichier de votre utilisateur est stocké dans Contoso Business, vous devez lui attribuer la valeur 2 pour les documents professionnels.  <br/> |
|**MicrosoftOfficeTermsOfUse** <br/> |Texte juridique pour déclarer que les informations que vous fournissez sont exactes conformément à nos conditions d'utilisation. Ce texte n'est pas visible par l'utilisateur. Il s'agit d'un accord entre vous, le fournisseur de l'application et Microsoft.  <br/> Consultez la rubrique suivante pour obtenir un exemple.  <br/> | String  <br/> | J'accepte les conditions indiquées sur la page [https://go.microsoft.com/fwlink/p/?LinkId=528381](third-party-applications-integrating-with-office-mobile-products.md) <br/> |
   
L’exemple de code suivant montre comment définir ces propriétés.
  
```cs
public static async Task SetExpandoProperties(StorageFile file,... other params ...) 
  { 
     var expandoProperties = new PropertySet(); 
     expandoProperties.Add("AppDisplayName", "Contoso",);  
     // String value. 
     expandoProperties.Add("MicrosoftOfficeOwnershipType", 1);  
     // Unit32 value - 1 (for personal), 2 (for business).  
     expandoProperties.Add("MicrosoftOfficeTermsOfUse", "I agree to the terms located at https://go.microsoft.com/fwlink/p/?LinkId=528381");   
    // String value. 
          
       var fileProperties = new PropertySet(); 
       fileProperties.Add("System.ExpandoProperties", expandoProperties); 
       await file.Properties.SavePropertiesAsync(fileProperties); 
  } 

```

## <a name="cached-file-updater-contracts"></a>Contrats de mise à jour des fichiers mis en cache

Si votre application universelle participe aux contrats de mise à jour des fichiers mis en cache, elle recevra les notifications des modifications apportées par une autre application universelle (comme Office) au fichier. Pour plus d'informations sur le fonctionnement dans Windows, voir la classe [CachedFileUpdater](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.cachedfileupdater.aspx).
  
Office utilise l'option **AllowOnlyReaders** pour ouvrir les fichiers en lecture et en écriture que votre application universelle fournit via les contrats de sélecteur de fichiers. Cela signifie que le fichier ne peut pas être déplacé, supprimé, renommé ou écrit par une autre application, y compris la vôtre, tant qu'il est ouvert dans Office. Office enregistre automatiquement le fichier, mais définit CachedFileManager.DeferUpdates pour empêcher l'activation de votre application jusqu'à ce qu'Office ferme le document, ou qu'Office soit suspendu par Windows (lorsque l'utilisateur bascule vers une autre application). Lorsqu'Office ferme le fichier, votre application peut écrire dans celui-ci. 
  
Votre application doit gérer toutes les communications avec votre service, y compris le téléchargement, l'actualisation et le chargement.
  
Le tableau suivant répertorie les paramètres à définir pour gérer les interactions entre votre application et Office.
  
|**Paramètre**|**Description**|
|:-----|:-----|
|[ReadActivationMode](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.readactivationmode.aspx) <br/> |Définissez **BeforeAccess** pour autoriser votre application à mettre à jour le fichier avant de l'envoyer à Office.  <br/> |
|[WriteActivationMode](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.writeactivationmode.aspx) <br/> |Définissez **ReadOnly** pour faire en sorte que le fichier soit en lecture seule. Définissez **AfterWrite** pour vous assurer que votre application sera déclenchée par l'élément CacheFileUpdater lorsqu'Office aura terminé d'utiliser le fichier.  <br/><br/>**REMARQUE :** si vous ne définissez pas **AfterWrite**, votre application ne sera pas notifiée des modifications, ce qui signifie que les modifications de l’utilisateur seront locales uniquement.           |
|[CachedFileOptions.RequireUpdateOnAccess](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.cachedfileoptions.aspx) <br/> |Définissez cette propriété pour vous assurer que votre application peut mettre à jour le fichier lorsqu’un utilisateur accède à la liste récente.  <br/> |
   
## <a name="invoking-office-from-your-app"></a>Appel d'Office à partir de votre application

Lorsqu'un utilisateur ouvre un document Office à partir de votre application, il peut être ouvert dans Excel Mobile, PowerPoint Mobile et Word Mobile. Par exemple, lorsqu'un utilisateur sélectionne un fichier \*.docx dans votre application, Word Mobile démarre avec le fichier \*.docx ouvert. L'application Office qui s'ouvre est basée sur l'application à laquelle l'utilisateur a associé le type du fichier.
  
Pour ouvrir un fichier à partir de votre application dans Office, nous vous recommandons d'utiliser **LaunchFileAsync()** afin de lancer le fichier. Nous vous déconseillons d'utiliser **LaunchUriAsync()** pour ce faire, car cela entrainera le lancement de l'application inscrite pour le schéma d'URI (le navigateur) au lieu d'Office. Toutefois, l'élément **LaunchUriAsync()** avec l'option **LauncherOptions.ContentType()** peut appeler Office, et dans ce cas, le fichier ouvert est marqué comme temporaire et est en lecture seule dans Office. 
  
Pour plus d'informations, voir la [classe Launcher](https://msdn.microsoft.com/library/windows/apps/windows.system.launcher.aspx).
  
## <a name="temporary-and-read-only-files"></a>Fichiers temporaires et en lecture seule

Définissez l'attribut **FILE_ATTRIBUTE_TEMPORARY** sur les fichiers temporaires et l'attribut **FILE_ATTRIBUTE_READONLY** sur les fichiers en lecture seule dans votre application. 
  
Les fichiers dont les attributs **FILE_ATTRIBUTE_TEMPORARY** ou **FILE_ATTRIBUTE_READONLY** sont définis s'ouvrent en lecture seule dans Office. L'attribut **FILE_ATTRIBUTE_TEMPORARY** empêche également le fichier d'apparaître dans la liste récente. 
  
Pour plus d'informations sur les attributs de fichier, voir la [fonction SetFileAttributes](https://msdn.microsoft.com/library/windows/desktop/aa365535%28v=vs.85%29.aspx).
  
## <a name="other-best-practices"></a>Autres méthodes conseillées

Pour optimiser la cohérence des fichiers, par exemple lorsque des erreurs ou des modifications conflictuelles se produisent, appliquez les meilleures pratiques suivantes :
  
- Évitez les conflits d'enregistrement.
    
  - Mettez le téléchargement sur pause en cas de conflit de serveur afin d'éviter la duplication (uniquement lorsqu'Office ne dispose plus de fichier ouvert en écriture). En règle générale, si un fichier provenant de votre application est ouvert dans Office, votre application est activée uniquement lorsqu'Office ferme ou est suspendu par Windows.
    
  - Si vous avez besoin de l’interface utilisateur pour gérer les conflits, implémentez les notifications toast. L’interface utilisateur n’est pas disponible dans son intégralité lorsqu’Office est suspendu.
    
- Gérez les erreurs.
    
  - Lorsqu’un verrou est libéré, informez les utilisateurs du conflit et indiquez un chemin pour résoudre ce problème dans votre application.
    
## <a name="see-also"></a>Voir aussi

- [Intégration à Office](integrate-with-office.md)   
- [Intégration à Office à partir de clients de synchronisation Win32](integrate-with-office-from-win32-sync-clients.md)
    

