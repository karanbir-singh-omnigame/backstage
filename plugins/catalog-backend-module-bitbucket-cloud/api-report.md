## API Report File for "@backstage/plugin-catalog-backend-module-bitbucket-cloud"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
import { BackendFeature } from '@backstage/backend-plugin-api';
import { CatalogApi } from '@backstage/catalog-client';
import { Config } from '@backstage/config';
import { EntityProvider } from '@backstage/plugin-catalog-backend';
import { EntityProviderConnection } from '@backstage/plugin-catalog-backend';
import { EventParams } from '@backstage/plugin-events-node';
import { Events } from '@backstage/plugin-bitbucket-cloud-common';
import { EventSubscriber } from '@backstage/plugin-events-node';
import { Logger } from 'winston';
import { PluginTaskScheduler } from '@backstage/backend-tasks';
import { TaskRunner } from '@backstage/backend-tasks';
import { TokenManager } from '@backstage/backend-common';

// @public
export class BitbucketCloudEntityProvider
  implements EntityProvider, EventSubscriber
{
  // (undocumented)
  connect(connection: EntityProviderConnection): Promise<void>;
  // (undocumented)
  static fromConfig(
    config: Config,
    options: {
      catalogApi?: CatalogApi;
      logger: Logger;
      schedule?: TaskRunner;
      scheduler?: PluginTaskScheduler;
      tokenManager?: TokenManager;
    },
  ): BitbucketCloudEntityProvider[];
  // (undocumented)
  getProviderName(): string;
  // (undocumented)
  getTaskId(): string;
  // (undocumented)
  onEvent(params: EventParams): Promise<void>;
  // (undocumented)
  onRepoPush(event: Events.RepoPushEvent): Promise<void>;
  // (undocumented)
  refresh(logger: Logger): Promise<void>;
  // (undocumented)
  supportsEventTopics(): string[];
}

// @alpha (undocumented)
export const bitbucketCloudEntityProviderCatalogModule: (
  options?: undefined,
) => BackendFeature;
```
