<template>
  <div id="app">
    <base-table :rows="rows">8
      <template #rows="{ row }">
        <base-table-row :row="row.jails">
          <template #row="{ jails }">
            <base-row-jails
              :jails="jails"
              :ellipsis="true"
            >
              <template #status="{ jail }">
                <base-badge
                  :status="jail"
                  :colors="{
                    'approved': 'green',
                    'pending': 'orange',
                    'reject': 'red'
                  }"
                />
              </template>
              <template #name="{ jail }">
                <span class="text-uppercase">{{ jail }}</span>
              </template>
              <template #createdAt="{ jail }">
                {{ jail }}
              </template>
              <template #index="{ jail }">
                <div class="d-flex table-index justify-content-center align-center ml-3">
                  {{ jail }}
                </div>
              </template>
            </base-row-jails>
          </template>
        </base-table-row>
      </template>
    </base-table>
  </div>
</template>

<script>
import BaseTable from "@/components/BaseTable";
import BaseTableRow from "@/components/BaseTableRow";
import BaseRowJails from "@/components/BaseRowJail";
import BaseBadge from "@/components/BaseBadge";

/**
 * TODO: Можно заюзать из репозитория
 * методы тестового задания для преобразования
 * юбого объекта под таблицы
 */
export default {
  name: 'App',
  components: {
    BaseBadge,
    BaseTable,
    BaseTableRow,
    BaseRowJails,
  },
  data() {
    return {
      rows: [
        {
          jails: [
            { index: 1 },
            { status: 'pending' },
            { name: "Andrew j." },
            { createdAt: new Date().toLocaleString() }
          ],
        },
        {
          jails: [
            { index: 1 },
            { status: 'pending' },
            { name: "Andrew j." },
            { createdAt: new Date().toLocaleString() }
          ],
        },
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Arial, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.table-index {
  min-width: 1.3rem;
  min-height: 1.3rem;
  border-radius: 1.3rem;
  background: #2c3e50;
  color: white;
}

.row  {
  display: flex;
  flex-wrap: nowrap;
}
</style>
