---
title: Bibliothèque JavaScript et référence REST pour Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 67b47b8b-d34b-4fad-af49-0c258c345ad2
description: La bibliothèque JavaScript et la référence REST pour Project Server 2013 contiennent des informations sur le modèle objet JavaScript et l’interface REST que vous utilisez pour accéder aux fonctionnalités de Project Server. Vous pouvez utiliser ces API pour développer des applications web entre navigateurs, des applications Project Professionnel 2013 et des applications pour les appareils non Windows qui accèdent à Project Server 2013 et Project Online.
ms.openlocfilehash: 43a689918d03634fc8752fdf64cf5f79ff27c269
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376489"
---
# <a name="javascript-library-and-rest-reference-for-project-server"></a>Bibliothèque JavaScript et référence REST pour Project Server

La bibliothèque JavaScript et la référence REST pour Project Server 2013 contiennent des informations sur le modèle objet JavaScript et l’interface REST que vous utilisez pour accéder aux fonctionnalités de Project Server. Vous pouvez utiliser ces API pour développer des applications web entre navigateurs, des applications Project Professionnel 2013 et des applications pour les appareils non Windows qui accèdent à Project Server 2013 et Project Online.
  
> [!NOTE]
> Le modèle objet JavaScript et l’interface REST s’alignent sur le modèle objet côté client (CSOM) Project Server. Ils fournissent des fonctionnalités équivalentes à l’espace de noms **Microsoft.ProjectServer.Client** dans le CSOM.
  
Vous pouvez accéder Project server par le biais du modèle objet JavaScript, qui est défini dans l’espace de noms [PS](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) dans le `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` fichier. [L’objet ProjectContext](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) dans l’espace [de noms PS](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) est le point d’entrée du modèle objet JavaScript.
  
> [!NOTE]
> Pour parcourir le modèle objet JavaScript et pour faciliter le débogage, vous pouvez utiliser le fichier PS.debug.js dans le même répertoire. Pour faciliter le développement sur un ordinateur distant, le téléchargement du [SDK Project 2013](https://www.microsoft.com/download/details.aspx?id=30435) inclut les assemblys .NET Framework pour le modèle CSOM et les fichiers PS.js et PS.debug.js.
  
Vous pouvez également accéder à Project server par le biais de l’interface REST. Le point d’entrée de l’interface REST est la **ressource ProjectServer** à `https://ServerName/pwaName/_api/ProjectServer` laquelle vous accédez à l’aide de l’URI du point de terminaison. Par exemple, la requête suivante obtient les affectations dans le projet spécifié (  _remplacez ServerName_ et  _pwaName_, puis modifiez le GUID pour qu’il corresponde à un projet).
  
`https://ServerName/pwaName/_api/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments`

La **ressource ProjectServer est** décrite dans les ressources [ProjectServer dans l’interface REST](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx#bk_ProjectServerResources). D’autres ressources REST sont décrites dans la documentation relative aux objets et membres JavaScript correspondants dans cette référence. Pour plus d’informations sur l’utilisation de REST, voir modèle objet côté [client (CSOM) pour Project Server](client-side-object-model-csom-for-project-2013.md) et programmation à l’aide du [service REST SharePoint 2013](https://msdn.microsoft.com/library/fp142385%28office.15%29.aspx).
  
## <a name="javascript-library-and-rest-reference-for-project-server"></a>Bibliothèque JavaScript et référence REST pour Project Server

<a name="pj15_JavaScriptAPIReference_PS"> </a>

- [PS.js bibliothèque JavaScript et référence REST](https://msdn.microsoft.com/library/5a140021-380a-d9e0-e36d-106df85f56d6%28Office.15%29.aspx) Contient des informations sur le modèle objet JavaScript et l’interface REST pour Project Server 2013.

## <a name="see-also"></a>Voir aussi

<a name="bk_addresources"> </a>

- [Documentation du développeur Project 2013](project-2013-developer-documentation.md)
- [Modèle objet côté client (CSOM) pour Project Server](client-side-object-model-csom-for-project-2013.md)
- [Mise en place du modèle objet JavaScript](getting-started-with-the-project-server-2013-javascript-object-model.md)  
- [Utilisation des projets avec le modèle objet JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)
