---
title: Écriture du code du serveur de formulaires
description: Décrit comment écrire du code serveur de formulaires dans Outlook 2013 et Outlook 2016, avec des documents de référence supplémentaires.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ff33badc-ceed-4364-b99c-8af3af83ceb6
ms.openlocfilehash: 3445dddd1899f01684a83bc547a7ab412db465e7
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894207"
---
# <a name="writing-form-server-code"></a>Écriture du code du serveur de formulaires

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Vous pouvez considérer un serveur de formulaires comme suit : 
  
- Programme Win32 qui affiche une interface et gère les messages Windows à l’aide des mécanismes de pompe de messages Windows standard.
    
- Objet qui inscrit sa fabrique de classes auprès d’OLE et est activé par les méthodes d’automatisation OLE.
    
- Objet MAPI qui suit les règles MAPI pour les interactions avec d’autres composants MAPI.
    
 Votre code doit gérer ces trois exigences générales simultanément. 
  
Pour plus d’informations sur l’inscription de la fabrique de classes de votre serveur de formulaires, consultez la section COM et ActiveX Object Services du Kit de développement logiciel (SDK) Windows. La gestion des messages Windows et l’affichage d’une interface sont des techniques de programmation Windows standard qui n’ont pas de spécifications particulières en ce qui concerne les formulaires MAPI. Là encore, le Kit de développement logiciel (SDK) Windows contient des détails sur la programmation Windows. Ce document contient ce que vous devez savoir pour implémenter les interfaces de formulaire MAPI requises et facultatives afin qu’elles suivent les règles MAPI pour les interactions avec d’autres composants MAPI, principalement le gestionnaire de formulaires MAPI et les applications clientes de messagerie.
  
Toutes les interfaces que vous pouvez utiliser lorsque vous implémentez des serveurs de formulaires sont dérivées , directement ou indirectement, de la classe de base OLE [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx). Cela signifie que toutes vos implémentations de ces interfaces doivent avoir des méthodes **QueryInterface**, **AddRef** et **Release** . Vous pouvez vous épargner beaucoup de travail si vous utilisez l’héritage multiple pour implémenter toutes les interfaces requises dans une nouvelle classe de votre propre, afin que toutes les interfaces que vous utilisez puissent partager une implémentation unique des méthodes **IUnknown** requises. Pour plus d’informations, consultez les méthodes [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) et [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) . Il n’existe aucune considération particulière concernant les serveurs de formulaires MAPI pour ces méthodes. 
  
Bien que toutes les interfaces de formulaire MAPI ne soient pas obligatoires pour tous les serveurs de formulaires, les méthodes d’une interface donnée sont obligatoires. Autrement dit, si vous choisissez d’implémenter une interface particulière, vous devez implémenter toutes les méthodes de l’interface. Cette situation est différente de celle de certains autres composants MAPI, tels que les transports de messages. Heureusement, les méthodes dans les interfaces de formulaire MAPI sont relativement simples, de sorte que l’implémentation de toutes ces méthodes n’impose pas une grande charge aux développeurs.
  
Les interfaces de formulaire MAPI sont indépendantes du type d’outil de développement utilisé pour créer un serveur de formulaires. Cela permet de créer des formulaires à l’aide de différents outils de développement. La seule exigence est que tous les serveurs de formulaires doivent prises en charge les interfaces de formulaire MAPI requises.
  
Toutes les interfaces MAPI liées aux formulaires ne sont pas requises par tous les serveurs de formulaires. Les interfaces facultatives vous permettent d’implémenter certaines fonctions de formulaire avancées qui ne sont pas nécessaires pour la plupart des serveurs de formulaires. Le tableau suivant répertorie les interfaces, ce pour quoi elles sont destinées et si vous devez les implémenter.
  
|**Interface**|**Description**|**État**|
|:-----|:-----|:-----|
|[IMAPIForm : IUnknown](imapiformiunknown.md) <br/> |Interface principale utilisée par les clients pour charger des serveurs de formulaires, exécuter des verbes de formulaire et arrêter les serveurs de formulaires. Il s’agit également de l’interface dérivée de **l’IUnknown** OLE utilisé pour informer d’autres composants OLE sur les interfaces implémentées par un objet de formulaire. |Requis  <br/> |
|[IPersistMessage : IUnknown](ipersistmessageiunknown.md) <br/> |Utilisé lors du chargement et de l’enregistrement des messages à partir d’objets de formulaire. |Requis  <br/> |
|[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) <br/> |Utilisé par les objets de formulaire pour suivre l’état du client de messagerie et déterminer si l’objet formulaire est capable d’afficher le message suivant ou précédent dans un dossier. |Facultatif  <br/> |
|[IClassFactory](https://msdn.microsoft.com/library/f624f833-2b69-43bc-92cd-c4ecbe6051c5%28Office.15%29.aspx) <br/> |Interface de fabrique de classe OLE utilisée par les objets de formulaire pour la conformité avec le mécanisme de fabrique de classes OLE. |Requis  <br/> |
|[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md) <br/> |Utilisé si votre serveur de formulaires prend en charge plusieurs types de formulaires. Dans ce cas, l’interface **IMAPIFormFactory** permet aux applications clientes d’accéder aux plusieurs interfaces **IClassFactory** (une par type de formulaire pris en charge par votre serveur de formulaires) que votre serveur de formulaire doit également implémenter. |Facultatif  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Développement de serveurs de formulaires MAPI](developing-mapi-form-servers.md)

